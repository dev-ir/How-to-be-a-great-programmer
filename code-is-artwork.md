# کد یک اثر هنری است

کد عالی باید آسان برای خواندن باشد. باگ‌ها باید به وضوح دیده شوند. به عنوان مثال:

```javascript
async function sendMessageToUser(userId, message) {
  const userId = 'abcd';
  const user = this.getUser(userId);
  await user.sendMessage(message);
}
```

می‌بینید که چگونه `userId` و `user` هم‌تراز هستند؟ حالا بیایید این را با یک تایپو ببینیم:

```javascript
async function sendMessageToUser(userId, message) {
  const userId = 'abcd';
  const user = this.getUser(userId);
  await usar.sendMessage(message);
}
```

بسیار واضح است. بیایید دوباره امتحان کنیم وقتی نام‌هایمان بصری هم‌تراز نیستند.

```javascript
async function sendMessageToUser(userId, message) {
  let user = this.getUser('abcd');
  const result = usar.sendMessage(message);
  await result;
}
```

خیلی سخت است که متوجه شویم.

حالا، نروید و `const` خود را به `let` تغییر دهید اگر منطقی نیست. اما وقتی فرصت دارید، متغیرها را هم‌تراز کنید تا کدتان ساده‌تر خوانده شود.

```javascript
async function sendMessageToUser(userId, message) {
  const userId = 'abcd';
  const user = this.getUser(userId);
  if ( !user ) throw new Error('Unknown User');
  await user.sendMessage(message);
}
```