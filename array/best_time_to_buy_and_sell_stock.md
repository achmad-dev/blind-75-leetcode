- use dynamic approach with oN
working code
```
/**
 * @param {number[]} prices
 * @return {number}
 */
var maxProfit = function(prices) {
    let min = prices[0]
    let max = 0
    for(let i = 1; i<prices.length; i++) {
        if(prices[i] < min) {
            min = prices[i]
        }
        if(prices[i] - min > max) {
            max = prices[i] - min
        }
    }
    return  max
};
```
