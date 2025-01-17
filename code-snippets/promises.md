<div align="center">
<h1>Promises</h1>
</div>

<ol>
<li>

**Promise is introduced in which version of JavaScript?**

- A: `ES5`
- B: `ES6`
- C: `ES8`
- D: `ES8`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

---

<li>

**When do we say that a promise is 'settled'?**

- A: `If it is fulfilled`
- B: `If it is rejected`
- C: `If it is pending`
- D: `If it is either fulfilled or rejected`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: D

</p>
</details>
</li>

---

<li>

**What will be the output?**

```JS
const validateUsernamePassword = (username, password) => {
	return new Promise((resolve, reject) => {
		if (username == "ABC" && password == "123") {
			resolve("SUCCESS!");
		} else {
			reject("FAILURE!");
		}
	});
};

validateUsernamePassword("ABC", "123")
	.then((msg) => {
		console.log(msg);
	})
	.catch((err) => {
		console.log(err);
	});
```

- A: `SUCCESS!`
- B: `FAILURE!`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

---

<li>

**While**

```JS
let setTimeoutResolveReject = new Promise((resolve, reject) => {
	setTimeout(() => {
		resolve("YES");
	}, 3000);
	setTimeout(() => {
		reject("NO")
	}, 2000);
});

setTimeoutResolveReject
.then((msg) => {
	console.log(msg);
})
.catch((err) => {
	console.log(err);
})
```

- A: `YES`
- B: `NO`
- C: `NO\nYES`
- D: `YES\nNO`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

---

<li>

**While execution, the random value of `randomWaitTime` generated was `3800`. What will be the output?**

```JS
let examplePromise = new Promise((resolve, reject) => {
	let timeout = 3000;
	let randomWaitTime = Math.floor(Math.random() * 5000) + 1;
	console.log(randomWaitTime);
	if (randomWaitTime <= timeout) {
		setTimeout(() => {
			resolve();
		}, randomWaitTime);
	} else {
		setTimeout(() => {
			reject();
		}, randomWaitTime);
	}
});

examplePromise
	.then(() => {
		console.log("RESOLVED!");
	})
	.catch(() => {
		console.log("REJECTED!");
	});
```

- A: `RESOLVED!`
- B: `REJECTED!`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

---

<li>

**Which of the following isn’t a method of Javascript Promise?**

- A: `Promise.then()`
- B: `Promise.all()`
- C: `Promise.error()`
- D: `Promise.catch()`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
</li>

---

<li>

**Which of the following isn’t a state of Javascript Promise?**

- A: `fulfilled`
- B: `awaited`
- C: `pending`
- D: `rejected`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

---

<li>

**What is the output?**

```JS
new Promise((resolve, reject) => {
  console.log(4)
  resolve(5)
  console.log(6)
}).then(() => console.log(7))
.catch(() => console.log(8))
.then(() => console.log(9))
.catch(() => console.log(10))
.then(() => console.log(11))
.then(console.log)
.finally(() => console.log(12))
```

- A: `4 6 7 9 11 12`
- B: `4 6 7 9 11 undefined 12`
- C: `4 6 8 12`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>


</ol>
