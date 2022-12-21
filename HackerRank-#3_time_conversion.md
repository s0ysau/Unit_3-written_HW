
```js
function timeConversion(s) {
    // Write your code here
    let Arr = s.split('')
    let hour = parseInt(s.split('').splice(0, 2).toString().replace(/,/g, ''))
    if (Arr[8] == "P" && hour < 12 ){
        let firDig = (parseInt(Arr[0]) + 1).toString()
        let secDig = (parseInt(Arr[1]) + 2).toString()
        Arr.splice(0, 1, firDig)
        Arr.splice(1, 1, secDig)
        let militaryTime = Arr.splice(0, 8).toString().replace(/,/g, '');
        return militaryTime
    } else if (Arr[8] == "P" && hour == 12 ){
        let militaryTime = Arr.splice(0, 8).toString().replace(/,/g, '');
        return militaryTime
    } else if (Arr[8] == "A" && hour == 12){
        let firDig = (parseInt(Arr[0]) - 1).toString()
        let secDig = (parseInt(Arr[1]) - 2).toString()
        Arr.splice(0, 1, firDig)
        Arr.splice(1, 1, secDig)
        let militaryTime = Arr.splice(0, 8).toString().replace(/,/g, '');
        return militaryTime
    } else if (Arr[8] == "A" && hour < 12){
        let militaryTime = Arr.splice(0, 8).toString().replace(/,/g, '');
        return militaryTime
    }
}
```

The way I approached this problem is first is to identify the elements in the array that will determine whether it is AM or PM and elements that need to change. so first, I would write a for loop to take the 8th element of the array that will seperate it between PM and AM. From there, I can add another condition that will determine whether the hour (Arr[0], Arr[1]) is either equal to 12 or less than 12. To do that, I created an hour variable to take the first two elements, turned it into integers and used that variable in the second in the loop condition. 

Then, if the array is PM and the hour equals 12 or if it is AM and hour is less than 12, the only thing that needs to be done is to remove the letters at the end and convert it into a string via inline callback function since there was no need to change the hour elements. 

For the arrays that is PM and less than 12 or AM equals 12 then I would take the first 2 elements, parseInt those elements then, if its PM add 1 & 2 and if its AM minus 1 & 2. Then the next step is to add those two elements back into the original array and convert that entire array into a string similar to before. 
