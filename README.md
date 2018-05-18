# redux-saga-sandbox
A console-based Redux Saga sandbox

## About
Use this tool to learn Redux Saga in a responsive, browser-based environment.

## Installation and Getting Started

Enusre you have installed `nodejs` from https://nodejs.org/. Something >= 6.x should be fine., You will also need to have a version of `npm` >= 5.2.

To install dependencies and start the application run the following commands:

`npm install`

`npm start`

Visit `http://localhost:8082` using Chrome

## Run in the console 
> var generator = function*() { return 5 } \
> generator() \
> generator().next() \


> var generator = function*() {
	yield 1;
	yield 2;
	yield 3;
	yield 4;
	yield 5;
} \
> var obj = generator() \
> obj.next() \
> obj.next() \
> obj.next() \
> obj.next() \
> obj.next() 


> var delayGenerator = function*() {
	yield new Promise(r => setTimeout(r, 1000));
	return 42;
} \
> let obj = delayGenerator() \
> obj.next().value.then(v => {
	console.log(obj.next())
}) \

> var delayGenerator = function*() {
	let data1 = yield delay(1000);
	console.log('Step 1');
	let data2 = yield delay(2000);
	console.log('Step 2');
	let data3 = yield delay(3000);
	console.log('Step 3');
}
 
> var obj = delayGenerator() \
> obj.next() \
> obj.next() \
> obj.next() \
> run(delayGenerator) \
> var wrapped = co.wrap(delayGenerator) \
> wrapped().then( v => console.log('Got a value', v) ); 






