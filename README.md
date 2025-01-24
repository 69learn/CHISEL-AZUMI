
نام پروژه : ریورس تانل Chisel - برقراری تانل بین چندین سرور با ایپی 4 و ایپی 6 

<div align="right">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/project-management.png" alt="Video Title" width="100">
  </a>
</div>
  </details>
</div>



**امکانات**
-----------------------
<div align="right">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/ability.png" alt="Video Title" width="100">
  </a>
</div>
  </details>
</div>

-----------------------
- ریورس تانل بین تک سرور و یا چندین سرور خارج و ایران
- ویرایش ریست تایمر ( ساعت یا دقیقه)
- پشتیبانی از TCP و UDP
- قابلیت تانل بر روی تک پورت و چندین پورت 
- امکان تانل بر روی 5 سرور خارج و یک سرور ایران و برعکس
- مناسب برای V2ray و Openvpn و Wireguard
- استفاده از ایپی 4 و ایپی 6 و هم چنین پرایوت ایپی
- ریستارت سرویس ها و kill در هر سی دقیقه
- ساختن keygen به صورت اتوماتیک برای ریورس تانل
- قابلیت مشاهده جداگانه تمامی سرویس ها
- امکان حذف تمامی تانل ها و سرویس ها
------------------------------------------------------
**نکات و اپدیت مهم**

- به این تانل دستور kill در هر سی دقیقه اضافه شد تا مشکلات دیسکانکت و max conn بهتر بشود.لطفا تست کنید
- میتوانید ریست تایمر را در edit menu بر طبق نیاز خودتون تنظیم کنید.( بسته به ترافیکی که مصرف میکنید، ریست تایمر را تغییر دهید یا بر اساس قطع شدن تانل)
- دستور bin bash برای سرور های ایرانی که مشکل اجرا نشدن دستور cron را داشتند، اضافه شد. برای کانفیگ دوباره، نخست uninstall کنید که دستورات cron پیشین پاک شود.
- بر روی سرورهاتون optimizer نصب کنید.
- اگر اختلالی داشتید لاگ سرویس هاتون را به صورت کامل برای من بفرستید .
```
cd /etc/systemd/system
ls
نام سرویس را بیابید و به جای سرویس نیم قرار بدید
systemctl status servicename
journalctl -u servicename.service
```


 ------------------------------------------------------
  <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/update.png" width="40" alt="Image"> </strong>آپدیت</summary>
  
  
------------------------------------ 

- اسکریپت برای تانل بین چندین سرور ایران به یک خارج، اپدیت شد. از این به بعد باید برای هر سرور ایران، پورت تانل جداگانه بدهید.
- ریست تایم با دستور KILL هر نیم ساعت به سرویس ها اضافه شد( بر طبق نیاز خودتان ویرایش کنید)
- امکان ویرایش ریست تایمر اضافه شد. ( دقیقه و ساعت)
- به اسکرین پایین نگاه کنید. به هنگام پرسش از شما در مورد تعداد کانفیگ (برای ریست تایم) ، تعداد کانفیگ خود را وارد نمایید. این کار برای ریست تایم نیاز میباشد. من دو عدد کانفیگ داشتم، پس عدد 2 را قرار دادم.
  
  </details>
</div>


--------------------

<div align="right">
  <details>
    <summary><strong>توضیحات</strong></summary>
  

- در این اسکریپت بوسیله ریورس تانل Chisel میخواهیم تانل را بین یک سرور و یا چندین سرور خارج و ایران، ایجاد کنیم.
- به طور مثال 3 سرور خارج دارید و بر روی هر کدام یک کانفیگ وایرگارد دارید، میتوانید آن ها را به یک سرور ایران وصل کنید و از یک سرور ایران برای 3 سرور خارجتان استفاده نمایید. این تانل ، توسط ریورس تانل انجام میشود.
- لطفا آموزش نوشتاری را با دقت بخوانید و با آزمون و خطا میتوانید تانل را با موفقیت ایجاد کنید.
- در این تانل پورت پیش فرضی استفاده نشده است
- خودم تمام روش ها را داخل سرور های مختلف تست کردم و جواب داده . بر روی دبیان 12 و اوبونتو 20 تست شده است.
- اگر از پنل v2ray استفاده میکنید و میخواهید با پرایوت ایپی، تانل را بسازید پس لطفا ایپی پرایوت ها را باز کنید.
- پنل شما در خارج باید نصب شده باشد
- کانفیگ ریورس تانل با پرایوت ایپی به صورت خودکار میباشد.اگر پاسخ خوبی نگرفتید با اسکریپت یا به صورت دستی تانل 6TO4 را انجام دهید و سپس تانل را برقرار کنید.
- لطفا برای کانفیگ دوباره، نخست از منوی uninstall اقدام به حذف تانل کنید تا مشکلی پیش نیاید یا همان کانفیگ را دوباره کانفیگ کنید.
- پاک کردن و کانفیگ دوباره، حتی یک دقیقه از وقت گران بهای شما را نخواهد گرفت پس نیاز به ویرایش دستی نمی باشد.
- در آخر هر کانفیگ، ایپی 4 سرور ایران شما با پورت نهایی نمایش داده میشود که با استفاده از آن در کلاینت وایرگارد یا V2ray میتوانید به اینترنت متصل شوید.
  
  </details>
</div>

 ------------------------------------------------------

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/warning.png" width="40" alt="Image"> </strong>نکات</summary>

- میتوانید از طریق tail /var/log/syslog درستی عملکرد cron را ببینید.
- این اسکریپت بارها تست شده و تمام گزینه هایش بدون مشکل کار میکند. سرویس ها هم ساخته میشود و کانفیگی هم از بین نمیرود. شما اختلال خود را با دستورات پایین بیابید
- اگر اختلالی در تانل داشتید همیشه وارد مسیر روبرو شوید cd /etc/systemd/system و با دستور ls ، سرویس های خارج و ایران را بیابید و با دستور systemctl status servicename و یا journalctl -u servicename.service ، دلیل اختلال تانل را بیابید.
- کسانی که تانلشون با تست سرعت در اسپید تست قطع میشه، من این مشکل را بررسی کردم و هم در صبح و هم در شب تست سرعت انجام دادم. تست سرعت در صبح بدون مشکل انجام شد اما تست سرعت در شب باعث قطعی تانل و ارتباط میشد ( بدون هیچ خطایی در لاگ تانل). این به این معنی هست که مشکل از تانل chisel نمی باشد و مشکل از جای دیگری است.
- شما میتوانید تست سرعت speedtest را در پنل خود ببندید که این مشکل در شب باعث قطعی تانل شما نشود.
- اگر سرعت شما پایینه ، حتما هم در سرور ایران و خارج، optimizer نصب کنید.
- **نکته** : **این مورد را دیدم چندین نفر به من گفتند. ببینید وقتی status داخل اسکریپت را نگاه میکنید هم سرور ایران و هم سرور خارج را نشان میدهد. به عبارتی در سرور ایران، وضعیت سرویس ایران سبر خواهد بود و در سرور خارج، وضعیت سرویس خارج سبز رنگ و اکتیو خواهد بود. در سرور خارج ، سرویس ایران غیرفعال میباشد و در سرور ایران، سرویس خارج غیرفعال میباشد.**
- اگر سرعت ریورس شما پایین امد، میتوانید x-ui یا پنل خود را هم یک بار ریست کنید


  </details>
</div>

------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/youtube.png" width="40" alt="Image"> ویدیوهای آموزشی</strong></summary>
------------------------------------  
- ویدیوی آموزشی توسط 69

<div align="right">
  <a href="https://www.youtube.com/watch?v=AjNrYOpNaQE">
    <img src="https://img.youtube.com/vi/AjNrYOpNaQE/0.jpg" alt="Video Title" width="300">
  </a>
</div>
<div align="right">
  <a href="https://www.youtube.com/watch?v=Avi8ErLPJJE">
    <img src="https://img.youtube.com/vi/Avi8ErLPJJE/0.jpg" alt="Video Title" width="300">
  </a>
</div>
  </details>
</div>


------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/guidelines.png" width="40" alt="Image"> </strong>پیش نیازها</summary>
  
  
------------------------------------ 

- لطفا سرور اپدیت شده باشه.
- ایپی 4 و 6 را فوروارد کنید و DNS های خود را نتظیم کنید. همه اینکار ها با optimizer انجام میشود.
- میتوانید از اسکریپت اقای [Hwashemi](https://github.com/hawshemi/Linux-Optimizer) و یا [OPIRAN](https://github.com/opiran-club/VPS-Optimizer) هم برای بهینه سازی سرور در صورت تمایل استفاده نمایید.
  </details>
</div>

----------------------------
**آموزش**
-



------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/script.png" width="40" alt="Image">اسکریپت های کارآمد</strong></summary>
------------------------------------   

**اسکریپت های کارآمد :**
- این اسکریپت ها optional میباشد.


 
 Opiran Script
```
apt install curl -y && bash <(curl -s https://raw.githubusercontent.com/opiran-club/VPS-Optimizer/main/optimizer.sh --ipv4)
```

Hawshemi script

```
wget "https://raw.githubusercontent.com/hawshemi/Linux-Optimizer/main/linux-optimizer.sh" -O linux-optimizer.sh && chmod +x linux-optimizer.sh && bash linux-optimizer.sh
```

------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/script.png" width="40" alt="Image">اسکریپت من</strong></summary>
------------------------------------   

- اسکریپت اصلی
```
sudo apt-get install python3 -y && apt-get install wget -y && apt-get install python3-pip -y && pip3 install colorama && pip3 install netifaces && apt-get install curl -y && python3 <(curl -Ls https://raw.githubusercontent.com/Azumi67/Chisel_multipleServers/main/chisel.py --ipv4)
```

- اگر با دستور بالا نتوانستید اسکریپت را اجرا کنید، نخست دستور زیر را اجرا نمایید و سپس دستور اول را دوباره اجرا کنید.
- اگر باز هم colorama رو نگرفت پس از اجرای دستور پایین ، همچنین این دستور هم اجرا کنید : pip3 install colorama , pip3 install netifaces

```
sudo apt-get install python-pip -y  &&  apt-get install python3 -y && alias python=python3 && python -m pip install colorama && python -m pip install netifaces
```

--------------------------------------
 <div dir="rtl">&bull;  دستور زیر برای کسانی هست که پیش نیاز ها را در سرور، نصب شده دارند</div>
 
```
python3 <(curl -Ls https://raw.githubusercontent.com/Azumi67/Chisel_multipleServers/main/chisel.py --ipv4)
```
--------------------------------------
 <div dir="rtl">&bull; اگر سرور شما خطای externally-managed-environment داد از دستور زیر اقدام به اجرای اسکریپت نمایید.</div>
 
```
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Azumi67/Chisel_multipleServers/main/managed.sh)"
```

---------------------------------------------



