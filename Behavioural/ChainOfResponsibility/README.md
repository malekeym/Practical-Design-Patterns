<div dir="rtl">
# هدف
Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain until an object handles it.

# ساختار
![UML](http://teddyma.cnblogs.com/images/cnblogs_com/teddyma/gof36.JPG)

# Participants
1. Handler
2. ConcreteHandler
3. Client

# مثال ۱
فرض کنید می‌خواهیم پرونده‌ای که رمزنگاری شده است را رمزگشایی کنیم. ما ۱۰ الگوریتم متفاوت برای رمزگشایی این پرونده طراحی کرده‌ایم. مسلماً بهترین راه این است که از الگوریتم‌های فراگیر، آسان و آن‌هایی که احتمال می‌دهیم زودتر پرونده‌مان را رمزنگاری می‌کنند شروع کنیم. بنابراین طبق سیاست‌هایی که داریم این ۱۰ الگوریتم را مرتب می‌کنیم. حال توسط `الگوی طراحی زنجیرهٔ پاسخگویی` این ۱۰ الگوریتم را به این پرونده اعمال می‌کنیم تا بالاخره یکی از این الگوریتم‌ها بتوانند پرونده‌مان را رمزگشایی کنند. توجه این که ممکن است هیچ کدام از این الگوریتم‌ها نتوانند پرونده را رمزگشایی کنند.

# مثال ۲
یک مثال معروف از الگوی طراحی زنجیرهٔ پاسخگویی، مبحث مدیریت استناء‌ها در زبان‌های برنامه‌نویسی شیء‌گرا مثل C++ و جاوا است.

# اطلاعات بیشتر
1. [پویش پرونده با فرمت‌های متفاوت](http://blog.sanaulla.info/2012/09/23/simple-example-to-illustrate-chain-of-responsibility-design-pattern/)
2. [مدیریت رایانامه‌های متفاوت](http://java.dzone.com/articles/design-patterns-uncovered-chain-of-responsibility)
3. [دو مثال خوب دیگر، شناسایی انوع پول و سکه و شناسایی اعداد](http://javapapers.com/design-patterns/chain-of-responsibility-design-pattern/)