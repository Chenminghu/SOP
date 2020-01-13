# Strategy Platform Optimization
> since this project is business sensitive, I can't show all the logic or code and will obscure part of picture I am going to show

This is a back-end engine which gives client ability to get real time position on open hedges. (this includes various contracts like Forward contract, Tarf, Knock In/Out contract, etc.) It enable clients to simulate the FX(Foreign Exchange) fluctuation VS the open position which helps them control the risk and manage their cash flow.

![SOP_ER_diagarm](https://user-images.githubusercontent.com/59182938/71923862-c0c59c00-3142-11ea-9a22-0cb30121f047.png)

This the ER Diagram of our Strategy Optimization Platform.

Four new entities are designed and created in this project
- Stategy
- Forecast
- Rolling_HedgeRatio
- Invoice

**Next, after creating all the tables, we need to write Insert/Delete/Update procedure for thoes table**

> Upsert/Delete procedure for sop.strategy
 
 **Few key features in this upsert procedure**
1.When customer book a strategy (UI interface will pass JSON code to us)  
SOP.Strategy, SOP.Forecast, SOP.Rolling_Hedgeratio will be filled respectively corresponding to the JSON code
If there is any error like missing data in JSON code, the procedure will automatically produce the error code and description of error
2.All three table use auto increase primary key.
3.There are also four keys for us to determine whether we should update three table or insert a new one.

> Update/Delete procedure for sop.forecast

Forecast table is able to auto rolling

> Update/Delete procedure for sop.Rolling

Nothing special

> Invoice/Update/Delete procedure for sop.Invoice

Nothing special

![sop1](https://user-images.githubusercontent.com/59182938/72283085-e6dfb600-35f2-11ea-914b-9cf08f6f4767.png)
![sop](https://user-images.githubusercontent.com/59182938/72283060-d3344f80-35f2-11ea-9aac-164cfbb8024e.png)

