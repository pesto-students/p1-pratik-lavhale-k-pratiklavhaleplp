Exercise 3.3 - What is the output of the below problem and why:
Code Snippet
function createIncrement() {
let count = 0;
function increment() {
count++;
}
let message = Count is ${count};
function log() {
console.log(message);
}
return [increment, log];
}
const [increment, log] = createIncrement();
increment();
increment();
increment();
log();

Output :-> Count is 0

Explaination :-> Reason for output is 'message' variable is only set once with the initial value of 'count' as 0 when 'createIncrement' is invoked. After three 'increment' invocation, count is '3' but log is console-ing 'message' which is 'Count is 0'. Hence final output is 'Count is 0'.