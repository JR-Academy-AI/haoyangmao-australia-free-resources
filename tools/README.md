# Local membership break-even module

Pure JavaScript; no dependencies, network, storage or paid APIs. Fee and spend must use the same billing period. uses represents permitted identical purchases. Set uncapped only when the terms explicitly have no cap.

```js
const {calculate}=require("./savings-calculator.cjs");
console.log(calculate({fee:8,spend:120,rate:10,cap:20,uses:1,uncapped:false}));
// {perUse:12,discount:12,fee:8,net:4}
```

Fictional arithmetic example, not a merchant offer. Amounts are rounded to cents; verify currency, terms, delivery and other costs separately. Zero and negative results are valid. Do not buy more to make the result positive.
