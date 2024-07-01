# ایجاد یک فایل Util

برای جلوگیری از وابستگی‌هایی مانند leftpad، تقریباً همیشه یک کلاس Util.js با روش‌های استاتیک مختلف که مفید هستند ایجاد می‌کنم. این کار مانع از جستجوی یک بسته برای مشکلات تک‌تابعی بی‌اهمیت می‌شود.

```javascript
module.exports = class Util {

  static async wait(delay) {
    return new Promise(resolve => setTimeout(resolve, delay));
  }

}
```
