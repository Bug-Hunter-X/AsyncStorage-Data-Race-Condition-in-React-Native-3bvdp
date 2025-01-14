# React Native AsyncStorage Data Race Condition
This repository demonstrates a common bug in React Native applications involving AsyncStorage and how to fix it using proper asynchronous programming techniques.

**The Bug:**
The `bug.js` file showcases a scenario where data is attempted to be accessed from AsyncStorage before it has finished being stored.  This leads to the application potentially trying to use an `undefined` value, resulting in unexpected behavior and possibly crashes.

**The Solution:**
The `bugSolution.js` file demonstrates the correct way to handle asynchronous operations with AsyncStorage, using `async/await` to ensure that the data is properly retrieved after it's been set.  This avoids the data race condition and prevents errors.

**How to Reproduce:**
1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run the `bug.js` example (it will error). 
4. Run the `bugSolution.js` example (it will work).

This demonstrates the importance of correctly handling asynchronous operations in React Native to prevent unexpected behavior.