
# Operators, Branching, Loops

## Easy

1. Write a program to add 5 numbers. The value of numbers are num1=5, num2=13, num3=7, num4=21 and num5=48.
```
  function add(num1,num2,num3,num4,num5){
    return num1+num2+num3+num4+num5
   }
   console.log(add(5,13,7,21,48))
 ////output---> 94
```
2. Write a program to take a number input from user and determine whether the number is odd or even.
```
  function oddOrEven(num){
    if(num%2===0){
        console.log("given input is even")
    }else{
        console.log("given input is odd")
     }
    }
 oddOrEven(5)
  ////output----> given input is odd
```

3. Write a program to find the maximum and minimum out of two given numbers. The numbers are num1=129 and num2=251.
```
function maxOrmin(num1,num2){
  if(num1>num2){
    console.log(`${num1} is greater than ${num2}`)
  }else{
     console.log(`${num2} is greater than ${num1}`)
  }

}
maxOrmin(129,251);
/// output--> 251 is greater than 129
```

4. Write a program to find the maximum out of three given numbers. The numbers are num1=8, num2=23 and num3=17.
 ```
   function findGreatest(num1,num2,num3){
    if(num1>num2&&num1>num3){
        console.log(`${num1} is the maximum in the given numbers ${num1}, ${num2}, ${num3}`)
    }else if(num2>num1&&num2>num3){
         console.log(`${num2} is the maximum in the given numbers ${num1}, ${num2}, ${num3}`)
    }else{
        console.log(`${num3} is the maximum in the given numbers ${num1}, ${num2}, ${num3}`)
    }

   }
   findGreatest(8,23,17)
 ////output----> 23 is the maximum in the given numbers 8, 23, 17
 ```

5. Write a program to find the minimum out of three given numbers. The numbers are num1=35, num2=29 and num3=46.
```
 function findSmallest(num1,num2,num3){
    if(num1<num2&&num1<num3){
        console.log(`${num1} is the smallest in the given numbers ${num1}, ${num2}, ${num3}`)
    }else if(num2<num1&&num2<num3){
         console.log(`${num2} is the smallest  in the given numbers ${num1}, ${num2}, ${num3}`)
    }else{
        console.log(`${num3} is the smallest  in the given numbers ${num1}, ${num2}, ${num3}`)
    }

   }
   findSmallest(35,29,46)
   ////output---->29 is the smallest  in the given numbers 35, 29, 46
```
 

6. Write program to take a month as an input from the user and find out whether the month has 31 days or not.
  ```
  function monthCheck(month){
    let months31 =["january", "march", "may", "july", "august", "october", "december"];
    if(months31.includes(month)){
      console.log(`${month} has 31 days.`)
    }else{
       console.log(`${month} does not have 31 days.`)
    }

  }
 monthCheck("january");      output----> january has 31 days.
 monthCheck("february")      output----> february does not have 31 days.
 monthCheck("march");        output----> march has 31 days.
 monthCheck("april");        output----> april does not have 31 days.
 monthCheck("may");          output----> may has 31 days.
 monthCheck("june");         output----> june does not have 31 days.
 monthCheck("july");         output----> july has 31 days.
 monthCheck("august");       output----> august has 31 days.
 monthCheck("september")     output----> september does not have 31 days.
 monthCheck("october")       output----> october has 31 days.
 monthCheck("november")      output----> november does not have 31 days.
 monthCheck("december")      output----> december has 31 days.
   
  ```

## Intermediate

7. Fizzbuzz - Write a program to return an array from 1 to 100. But for every multiple of 3, replace the number with "Fizz", for every multiple of 5, replace the number with "Buzz" and for every multiples of 3 & 5, replace with "FizzBuzz".

    Your output should look something like this `1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, FizzBuzz, 16, 17 ..... `

 ```
  function printer(){
     let arr=[];
  for(let i =1; i<=100; i++){
    if(i%3===0&&i%5===0){
      arr.push("FizzBuzz")
    }else if(i%5===0){
      arr.push("Buzz")
    }else if(i%3===0){
      arr.push("Fizz")
    }else{
      arr.push(i)
    }        
  }
  return arr
}
console.log(printer())
 
 ////output---->
 [
  1,      2,      'Fizz',     4,      'Buzz', 'Fizz',
  7,      8,      'Fizz',     'Buzz', 11,     'Fizz',
  13,     14,     'FizzBuzz', 16,     17,     'Fizz',
  19,     'Buzz', 'Fizz',     22,     23,     'Fizz',
  'Buzz', 26,     'Fizz',     28,     29,     'FizzBuzz',
  31,     32,     'Fizz',     34,     'Buzz', 'Fizz',
  37,     38,     'Fizz',     'Buzz', 41,     'Fizz',
  43,     44,     'FizzBuzz', 46,     47,     'Fizz',
  49,     'Buzz', 'Fizz',     52,     53,     'Fizz',
  'Buzz', 56,     'Fizz',     58,     59,     'FizzBuzz',
  61,     62,     'Fizz',     64,     'Buzz', 'Fizz',
  67,     68,     'Fizz',     'Buzz', 71,     'Fizz',
  73,     74,     'FizzBuzz', 76,     77,     'Fizz',
  79,     'Buzz', 'Fizz',     82,     83,     'Fizz',
  'Buzz', 86,     'Fizz',     88,     89,     'FizzBuzz',
  91,     92,     'Fizz',     94,     'Buzz', 'Fizz',
  97,     98,     'Fizz',     'Buzz'
]
 
 ```


8. Print the following star pattern :-

    \* \
    \* \* \
    \* \* \* \
    \* \* \* \* \
    \* \* \* \* \* 

    ```
    function printStar(){
     let pattern=""

         for(let i=0;i<=4;i++){
    pattern+="* "
    console.log(pattern)
     }
   }

   printStar()

   ///output---> * 
                  * * 
                  * * * 
                  * * * * 
                  * * * * * 
    
    ```

9. Write a program to take a number input from user and print multiplication table 12 times for that number.

10. Write a program to return a Fibonacci series : 0,1,1,2,3,5,8,13,21....

11. Write a program to take an input from a user and find its Factorial.
   `Example: Factorial of 5 is 120`
12. Write a Program to take a number input from user and find if the number is Prime or not.

13. Write a program to take a day as an input and determine whether it is a weekday or weekend.
   `Example: Tuesday is weekday.`