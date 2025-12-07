# 121._Best_Time_to_Buy_and_Sell_Stock
# You are given an array prices where prices[i] is the price of a given stock on the ith day. 
# You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.  
# Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int mini=INT_MAX;
        int maxProfit=0;
        for(int i=0;i<prices.size();i++){
            if(prices[i]<mini){
                mini=prices[i];
            }
            int profit=prices[i]-mini;
            if(profit>maxProfit){
                maxProfit=profit;
            }
        }
        return maxProfit;
    }
};
