# StockTrader-Java
public class StockTrader {
    public static int maxProfit(int[] prices){
        int minPrice = Integer.MAX_VALUE;
        int maxProfit = 0;
        for(int price : prices){
            if(price < minPrice){
                minPrice = price;

            } else if(price - minPrice > maxProfit){
                maxProfit = price - minPrice;
            }
        }
        return maxProfit;


    }
    public static void main(String[] args) {
        int[] prices = {7,1,5,3,6,4};
        System.out.println("Max Profit:" + maxProfit(prices));
    }
   
}
//find the output in this code through 
- Buy at ₹1 (lowest price before a rise)
- Sell at ₹6 (highest price after ₹1)
- Profit = ₹6 - ₹1 = ₹5
✅ Final Output
System.out.println("Max Profit: " + maxProfit(prices)); // Output: Max Profit: 5


