
Understand what forEach does

Write our own version of the forEach function

Why Do I Need To Know This?

Write cleaner and more declarative code

Use built in higher order functions and callback functions Foundation for modern libraries and frameworks

forEach Loops through an array, Runs a callback function for each value in the array and then returns undefined

forEach will always return undefined - no matter what



An Example

let arr = [1,2,3];

arr.forEach(function(value, index, array){

  console.log(value);
  
});

// 1

// 2

// 3

// undefined




Let’s Build Our Own!


Loops through an array,

Runs a callback function on each value in the array,

returns undefined

function forEach(array, callback){

  for(let i = 0; i < array.length; i++){
  
    callback(array[i], i, array);
  }
}

An Example

function countZeroes(arr){

  let total = 0;
  
  arr.forEach(function(val){
  
    if(val === 0) {
    
        total++;
        
    }
    
  });
  
  return total;
  
}

countZeroes([2,4,6]); // 0

countZeroes([0,1,2,0,1]); // 2

Remember - forEach always returns undefined!



When You Would Use forEach

You want to iterate over an array, but the return value of your callback is not important

Almost all of the time there are better options…


Recap

forEach iterates over an array, runs a callback on each value and

forEach returns undefined
