> The server and the web browser communicate with each other using the HTTP protocol. The Network tab shows how the browser and the server communicate.

---

**<u>_sync and async_</u>** :

> There are two ways in which the callback may be called: synchronous and asynchronous. Synchronous callbacks are called immediately after the invocation of the outer function, with no intervening asynchronous tasks, while asynchronous callbacks are called at some point later, after an asynchronous operation has completed.

-   Understanding whether the callback is synchronously or asynchronously called is particularly important when analyzing side effects

**_to understand sync and async check the following example:_**

```javascript
let value = 1;

doSomething(() => {
    value = 2;
});

console.log(value);
```

**_notice: this part `() => { value = 2; }` is a callback function_**

If `doSomething` calls the callback synchronously, then the last statement would log `2` because `value = 2` is synchronously executed; otherwise, if the callback is asynchronous, the last statement would log `1` because `value = 2` is only executed after the console.log statement.

**_question to ask in this part !!_**

> **_How Do We Know if doSomething is Sync or Async?_**
> If doSomething is a regular function that immediately executes the callback, it is synchronous.
> If doSomething uses mechanisms like setTimeout, Promise, or I/O operations to defer the callback execution, it is asynchronous.

---

**_<u>DOM</u>_**

**_DOM:is an API enables programmatic modification of the element trees corresponding to web pages_**

> **_In HTML DOM (Document Object Model), every element is a node_**

-   All HTML elements are element nodes.
-   All HTML attributes are attribute nodes.
-   Text inserted into HTML elements are text nodes.
