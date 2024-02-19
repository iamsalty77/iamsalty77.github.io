---
layout: post
title:  "NVL, NULLIF"
date:   2024-02-14 21:06:18 +0900
categories: jekyll update
---
NVL은 NULL 값을 다른 값으로 대체하는 데애 사용됩니다. NVL은 두 개의 인자를 가지며,

첫번째 인자가 NULL이 아니면 해당 값을 반환하고, NULL이라면 두번째 인자로 지정된 값을 반환합니다.

예를 들어,

{% highlight ruby %}
SELECT NVL(column1, 0)
AS result
FROM your_table;

{% endhighlight %}

여기서 column1 이 NULL 인 경우 0을 반환하고 NULL 이 아니면 column1을 그대로 반환한다.

NULLIF는 두개의 표현식을 비교하여 두 값이 동일하면 NULL 을 반환, 그렇지 않으면 첫번째 표현식의 값을 반환합니다.

예를 들어,

{% highlight ruby %}
SELECT NULLIF(column1, column2)
AS result
From your_table;

{% endhighlight %}

여기서 column1과 column2가 같을 경우 NULL을 반환하고 다른 경우 column1 을 반환합니다.