
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


