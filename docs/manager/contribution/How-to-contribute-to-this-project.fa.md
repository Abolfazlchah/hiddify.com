---
title: چگونه می‌توان در این پروژه همکاری نمود
---

# چگونه می‌توان در این پروژه همکاری نمود
برای این کار کافیه شما git را روی سیستم خود نصب نمایید.

## نصب git روی سیستم 
بر اساس سیستم عامل خود یکی از موارد زیر را باز نمایید.
<details dir=rtl markdown="1"><summary><h3>ویندوز</h3></summary>

- ابتدا به [اینجا](https://git-scm.com/download/win) بروید و نسخه مخصوص ویندوز را دانلود کنید.
- سپس فایل دانلود شده را از حالت فشرده خارج نمایید و برای نصب آن را ارا نمایید.
<div align=center markdown="1">

<img alt="location-git-windows-download" src="https://github.com/hiddify/Hiddify-Manager/assets/125398461/cd883726-f340-441c-bbca-df98f0389de2" />

</div>

- سپس wizard نصب را تا انتها با next و yes دنبال کنید. پیشنهاد می‌شود تنظیمات دیفالت را تغییر ندهید.

<div align=center markdown="1">

<img alt="read-and-accept-git-license-agreement" src="https://github.com/hiddify/Hiddify-Manager/assets/125398461/c8220a90-4f88-451f-ac60-ca6280feef20" />

</div>
به صورت دیفالت محل نصب git در این مسیر است.
<div dir=ltr>

```
C:/Program Files/Git
```
</div>
یعنی در مراحل بعد، پروژه‌ها در این مسیر قرار می‌گیرند. کار تمام است.
- برای چک کردن ورژن `git` نصب شده، `command prompt` را باز نمایید و دستور زیر را اجرا کنید.

<div dir=ltr>

```
git version
```

</div>

- به صورت دیفالت `git` در پوشه `Home` کاربر نصب می‌گردد.
</details>

<details dir=rtl markdown="1"><summary><h3>مک</h3></summary>

- ابتدا از [اینجا](https://sourceforge.net/projects/git-osx-installer/files/git-2.23.0-intel-universal-mavericks.dmg/download?use_mirror=autoselect) فایل نصب را دانلود کنید.
- سپس آن را جارا نمایید. نصب خیلی ساده‌ای دارد.
- بعد از نصب برای چک کردن ورژن `git` نصب شده، `terminal` را باز نمایید و دستور زیر را اجرا کنید.

<div dir=ltr markdown="1">

```
git version
```

</div>


</details>

<details dir=rtl  markdown="1"><summary><h3>لینوکس</h3></summary>

در اکثر توزیع‌های سیستم عامل لینوکس git به صورت دیفالت نصب است و نیاز نیست کار خاصی بکنید. اما اگر به هر دلیلی نیاز بود آن را نصب نمایید باید سرچ بزنید و کامند مناسب مربوط به آن توزیع را پیدا کنید. در ادامه کامند نصب مربوط به ند توزیع معروف قرار می‌گیرد.
<div dir=ltr>

**Debian/Ubuntu**

```
sudo apt-get install git-all
```

**Fedora**

```
dnf install git-all
```

**Arch**
````
pacman -Syu git-all
````
</div>

در همه توزیع‌ها git در مسیر Home کاربر نصب می‌گردد.
- برای چک کردن نسخه git نصب شده در ترمیال این دستور را اجرا کنید.

<div dir=ltr>

```
git version
```
</div>

</details>




## استفاده از git جهت توسعه پروژه هیدیفای‌منیجر

- ابتدا باید پروژه را fork کنید. برای این کار اگر قصد fork کردن پنل را دارید کامند زیر را اجرا کنید.

<div dir=ltr>

```
git clone https://github.com/hiddify/HiddifyPanel.git
```

</div>

اگر قصد fork کردن Hiddify-Manager را دارید، دستور زیر را اجرا کنید.

<div dir=ltr>

```
git clone https://github.com/hiddify/Hiddify-Manager.git
```

</div>

برای سایر repository ها نیز به همین شکل کافیه که وارد repository شوید و روی `Code` بزنید و در تب `Local` آدرس قرار گرفته شده در‌ `HTTPS` را کپی کنید و در دستور بالا قرار دهید.

<div align=center markdown="1">

<img src="https://github.com/hiddify/Hiddify-Manager/assets/125398461/483dde4e-e4fd-470a-be94-552d5c72c2a8" />

</div>

- اندکی صبر کنید تا فایل‌های پروژه کپی شود.

<div align=center markdown="1">

<img src="https://github.com/hiddify/Hiddify-Manager/assets/125398461/b4730f3a-3f86-4792-8ccc-6a5789056c1d" />

</div>

- حالا باید یک شاخه یا branch از پروژه درست کنید تا روی آن کار کنید. برای این کار ابتدا برای شاخه یک اسم انتخاب کنید. مثلا فرض کنیم اسم شاخه را `Hiddify-develop` انتخاب می‌کنیم. حالا دستورات زیر را اجرا کنید. 

<div dir="ltr" >

```
git branch Hiddify-develop
git checkout Hiddify-develop
```

</div>

<div dir="rtl" >

-  حالا تغییرات مورد نظر خود را روی فایل‌ها با استفاده از هر ابزاری اعمال کنید. توصیه می‌شود از `VSCode` استفاده نمایید.
-  یادتون نره مسیر تمامی فایل‌ها در پوشه‌های گفته شده در مرحله نصب است.
- 
- حالا وقتی تغییرات مورد نظر خود را اعمال نمودید باید تغییرات را در `git` نیز ثبت کنید. بنابراین در ترمینال کامند‌های زیر را به ترتیب اجرا نمایید.
- ابتدا با کامند زیر انجام تغییرات را به `git` اعلام کنید.


<div dir=ltr>

```
git add
```

</div>

- سپس تغییرات را کامیت نمایید. نیاز است که در اینجا یک توضیح برای تغییرات اعلام نمایید.

<div dir=ltr>

```
git commit -m "a short description of the change"
```

</div>

مثلا اگر تغییرات مدنظر شما مربوط به بخش توسعه بات باشد می‌توان چنین توضیحی نوشت.


<div dir=ltr>

```
git commit -m "add some features to the telegram bot"
```

</div> 

هیچ مشکلی ندارد که توضیحات این بخش زیاد باشد و اتفاقا توصیه می‌شود تا جای ممکن توضیحات کامل و جامع باشد.
در این مرحله تغییرات با موفقیت وارد سیستم git شد. حالا باید تغییرات را به سمت GitHub بفرستید. برای این کار دستور زیر را اجرا کنید. 

<div dir=ltr>

```
git push
```
</div>

در اینجا مشخصات اکانت شما در گیتهاب پرسیده می‌شود. نیاز است `Username` و `Password` خود در گیتهاب را وارد نمایید.


- حالا وارد اکانت خود در گیتهاب شوید و پروژه فورک شده را باز نمایید.
مسیری به شکل زیر دارد:

<div dir=ltr markdown="1">

`https://github.com/<your_username>/Hiddify-Manager`

</div>

- حالا یک banner مشاهده می‌کنید که به شما اعلام می‌کند که branch شما از پروژه اصلی یک مرحله جلوتر است. برای اینکه تغییرات با پروژه اصلی merge یا ادغام شود `Contribute` را کلیک کنید و `Open a pull request` را بزنید.
- کار تمام است تغییرات به پروژه ارسال شد. حالا پس از تایید مدیر پروژه تغییرات شما به پروژه اضافه می‌گردد.

