# Strategy Platform Optimization
> since this project is business sensitive, I can't show the code and will obscure part of picture I am going to show

This is a back-end engine which gives client ability to get real time position on open hedges. (this includes various contracts like Forward contract, Tarf, Knock In/Out contract, etc.) It enable clients to simulate the FX(Foreign Exchange) fluctuation VS the open position which helps them control the risk and manage their cash flow.

![SOP_ER_diagarm](https://user-images.githubusercontent.com/59182938/71923862-c0c59c00-3142-11ea-9a22-0cb30121f047.png)

This the ER Diagram of our Strategy Optimization Platform.

Four new entities are designed and created in this project
- Stategy
- Forecast
- Rolling_HedgeRatio
- Invoice

Next, after creating all the tables, we need to write Insert/Delete/Update procedure for thoes table

> Upsert/Delete procedure for sop.strategy
  The concept is when customer book a strategy (UI interface will pass JSON code to us)  SOP.Strategy, SOP.Forecast, SOP.Rolling_Hedgeratio will be filled respectively corresponding to the JSON code
  
> Update/Delete procedure for sop.forecast

> Update/Delete procedure for sop.Rolling
