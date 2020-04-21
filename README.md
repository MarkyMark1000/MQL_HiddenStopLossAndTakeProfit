<h2>MQ4 - HiddenSLandTP:</h2>

<h4>Inputs:</h4>

input int I_StopLoss_Points=50;           //Desired StopLoss in points.<br>
input int I_TakeProfit_Points=50;         //Desired TakeProfit in points.<br>
input RelativePrice I_Relative=OpenPrice; //Use OpenPrice or Mid when calculating StopLoss or TakeProfit.<br>
input bool I_DrawLines=True;              //Draw Lines on Chart.<br>
input int I_Slippage=5;                   //Slippage used when closing the trades.<br>

<h4>Description:</h4>

This Expert Advisor is a very basic Hidden StopLoss and TakeProfit System.<br>

Firstly, a trade must be entered onto the chart, preferably with a large stoploss and takeprofit value.<br>

This EA can then be dragged onto the chart.   It will scan through the active trades associated with the Chart's symbol and then defines a
a hidden stoploss and hidden takeprofit using the inputs I_StopLoss_Points, I_TakeProfit_Points and I_Relative.   I_Relative indicates
if the OpenPrice of the trades should be used to define the hidden stoploss level or the mid of the candle.<br>

It can draw lines onto the chart to incidate where the hidden stoploss and takeprofit are if required, however these lines are not dynamic
and will need to be removed upon completion.<br>

I_Slippage indicates the slippage used when closing the trades.<br>

This is only a basic system and it does not deal with the more dynamic features of MetaTrader such as StopLevel, FreezeLevel, Limit orders,
StopOrders, the addition of trades after the EA has been initated or changes to the instrument id when position sizes are adjusted.<br>

As an example, lets say you had a spread of 20 points, but the spread had a tendancy to jump up to 60 points or there is a 60 point stoplevel
on the symbol.   You could add a trade with stoploss and takeprofit in excess of say 200 points and then add a hidden stoploss
and take profit of say 60 points without needing to worry about the stop hunting or the stoplevel.   If however the EA stops working or you
lose connection to the server, then your positions become more vulnerable to large losses.