---
title: مارک‌داون
weight: 2
---

Hugo از سینتکس [مارک‌داون](https://en.wikipedia.org/wiki/Markdown) برای قالب‌بندی متن، ایجاد فهرست و موارد دیگر پشتیبانی می‌کند. این صفحه برخی از رایج‌ترین نمونه‌های سینتکس مارک‌داون را به شما نشان می‌دهد.

<!--more-->

## مثال‌های مارک‌داون

### ظاهر طراحی دادن به متن

| سبک   | سینتکس     | مثال   | خروجی   |
| --------  | -------- | ------ | ------ |
| توپر | `**متن توپر**` | `**متن توپر**` | **متن توپر** |
| کج | `*متن کج*` | `*متن کج*` | *متن کج* |
| خط خورده | `~~متن خط خورده~~` | `~~متن خط خورده~~` | ~~متن خط خورده~~ |
| پایین‌نویس | `<sub></sub>` | `این یک متن <sub>پایین‌نویس</sub> است` | این یک متن <sub>پایین‌نویس</sub> است |
| بالانویس | `<sup></sup>` | `این یک متن <sub>بالانویس</sub> است` | این یک متن <sub>بالانویس</sub> است |

### بلوک نقل‌قول

بلوک نقل‌قول با ذکر منبع

> با اشتراک‌گذاری حافظه ارتباط برقرار نکنید، حافظه را با برقراری ارتباط به اشتراک بگذارید.<br>
> — <cite>راب پایک[^1]</cite>

[^1]: نقل‌قول بالا گزیده‌ای از [سخنرانی](https://www.youtube.com/watch?v=PAAkCSZUG1c) راب پایک در Gopherfest، در تاریخ ۲۷ آبان ۱۳۹۴ است.

### جدول‌ها

جدول‌ها بخشی از مشخصات اصلی مارک‌داون نیستند، اما Hugo از آنها در خارج از جعبه پشتیبانی می‌کند.

   نام | سن
--------|------
    گودرز | ۳۰
  آصف | ۳۴

#### مارک‌داون درون‌خطی درون جدول‌ها

| کج   | توپر     | کد   |
| --------  | -------- | ------ |
| *کج* | **توپر** | `کد` |

### بلوک‌های کد

{{< cards >}}
  {{< card link="../../guide/syntax-highlighting" title="برجسته‌کردن سینتکس" icon="sparkles" >}}
{{< /cards >}}

### فهرست‌ها

#### فهرست مرتب‌شده

1. اولین آیتم
2. دومین آیتم
3. سومین آیتم

#### فهرست مرتب‌نشده

* فهرست آیتم
* یک آیتم دیگه
* و یک آیتم دیگه

#### فهرست تو در تو

* میوه
  * سیب
  * پرتقال
  * موز
* لبنیات
  * شیر
  * پنیر

### عکس‌ها

![](https://source.unsplash.com/featured/800x600?landscape)

با توضیحات:

![](https://source.unsplash.com/featured/800x600?landscape "یک چشم‌انداز Unsplash")

## پیکربندی

Hugo از [Goldmark](https://github.com/yuin/goldmark) برای تجزیه مارک‌داون استفاده می‌کند.
 رندر مارک‌داون را می‌توان در `hugo.yaml` تحت `markup.goldmark` پیکربندی کنید.
 در زیر پیکربندی پیش‌فرض هگزترا را می‌توانید ببینید:

```yaml {filename="hugo.yaml"}
markup:
  goldmark:
    renderer:
      unsafe: true
  highlight:
    noClasses: false
```

برای گزینه‌های پیکربندی بیشتر، به مستندات Hugo در [پیکربندی نشانه‌گذاری](https://gohugo.io/getting-started/configuration-markup/) مراجعه کنید.

## منابع یادگیری

* [راهنمای مارک‌داون](https://www.markdownguide.org/)
* [برگه تقلب مارک‌داون](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [آموزش مارک‌داون](https://www.markdowntutorial.com/)
* [مرجع مارک‌داون](https://commonmark.org/help/)