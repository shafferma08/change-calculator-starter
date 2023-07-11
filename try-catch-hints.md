1. **Understand the problem**: Before beginning to code, make sure you understand the problem. In this case, you need to handle a user error when the cash amount given is less than the bill. If this occurs, the program should stop and display an error message.

2. **Identify where to add the code**: The instructions tell you to add a try-catch statement to the `runTheRegister()` function in `script.js`. Make sure you know where this function is in your code.

3. **Write the try statement**: Within the try statement, you're checking if `changeValue` is not greater than or equal to zero. `changeValue` is the difference between the cash amount and the bill. If it's not greater than or equal to zero, it means the cash amount doesn't cover the bill. In this case, you should `throw` an error message.

   Hint: The code for this would look something like this:
   ```javascript
   if (!(changeValue >= 0)) {
      throw "Cash amount doesn't cover the bill";
   }
   ```

4. **Run the commands**: If the cash amount does cover the bill, then you can continue running the rest of the function. Specifically, you want to format the change and calculate the change.

   Hint: The code for this would look like this:
   ```javascript
   changeBox.value = formatCurrency(changeValue);
   calcChange(changeValue);
   ```

5. **Write the catch statement**: The catch statement is where you handle the error if one is thrown. In this case, you're instructed to set the `innerHTML` of the element with the id `warning` to the value of the thrown exception. 

   Hint: The code for this would look like this:
   ```javascript
   document.getElementById("warning").innerHTML = error;
   ```

6. **Put it all together**: Once you've written the try and catch statements, you need to put it all together in a try-catch statement. Make sure you've placed the try-catch statement in the correct place within the `runTheRegister()` function. 

   Hint: The full try-catch statement would look like this:
   ```javascript
   try {
      if (!(changeValue >= 0))
         throw "Cash amount doesn't cover the bill";
      changeBox.value = formatCurrency(changeValue);
      calcChange(changeValue);
   } catch(error) {
      document.getElementById("warning").innerHTML = error;
   }
   ```

7. **Test your code**: After you've added the code, make sure to test it to see if it works correctly. Try inputting a cash amount that is less than the bill and see if you get the correct error message. Then, input a cash amount that covers the bill and see if the function works as expected. 

Remember, coding is often a process of trial and error. It's okay if you don't get it right the first time. Keep trying and you'll get there!
