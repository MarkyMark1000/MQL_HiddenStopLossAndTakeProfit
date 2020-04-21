MQ4

HiddenSLandTP:

Inputs:

input int I_StopLoss_Points=50;           //Desired StopLoss in points.
input int I_TakeProfit_Points=50;         //Desired TakeProfit in points.
input RelativePrice I_Relative=OpenPrice; //Use OpenPrice or Mid when calculating StopLoss or TakeProfit.
input bool I_DrawLines=True;              //Draw Lines on Chart.
input int I_Slippage=5;                   //Slippage used when closing the trades.

This Expert Advisor is a very basic Hidden StopLoss and TakeProfit System.

Firstly, a trade must be entered onto the chart, preferably with a large stoploss and takeprofit value.

This EA can then be dragged onto the chart.   It will scan through the active trades associated with the Chart's symbol and then defines a
a hidden stoploss and hidden takeprofit using the inputs I_StopLoss_Points, I_TakeProfit_Points and I_Relative.   I_Relative indicates
if the OpenPrice of the trades should be used to define the hidden stoploss level or the mid of the candle.

It can draw lines onto the chart to incidate where the hidden stoploss and takeprofit are if required, however these lines are not dynamic
and will need to be removed upon completion.

I_Slippage indicates the slippage used when closing the trades.

This is only a basic system and it does not deal with the more dynamic features of MetaTrader such as StopLevel, FreezeLevel, Limit orders, 
StopOrders, the addition of trades after the EA has been initated or changes to the instrument id when position sizes are adjusted.