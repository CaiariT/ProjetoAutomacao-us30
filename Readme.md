// TESTES A SEREM REALIZADOS:

//TESTAR ABRIR OPERAÇÃO NO 5 OU NO 1 MIN
 
 // ANALISAR -> BARRA DE STOP, ATRAS DA ULTIMA BARRA DOS 5 MIN
// DAR ESPAÇO ENTRE A BARRA E O STOP - 100 PIPS?






//+------------------------------------------------------------------+
//|                                                    Anotações.mq5 |
//|                                           Copyright 2022, Teste.api |
//|                                          https://www.caiaritolotti.com/ |
//+------------------------------------------------------------------+
#property copyright "Copyright 2022, teste.api"
#property link      "https://www.caiaritolotti.com/"
#property version   "Version = 1.01"


#include <Trade\Trade.mqh>

CTrade dayTrade;
input int loss = null;
input int gain = null;
input string inicio =  ;
input string termino = ;
input string fechamento = ; 
input int contratos = 0.01;
input int media = 20;


MqlDateTime horario-inicio, horario_termino, horario_fechamento, horario_atual, dia;










//+------------------------------------------------------------------+
//| Expert initialization function                                   |
//+------------------------------------------------------------------+
int OnInit() 
{
//--- create timer
   EventSetTimer(60);
   
//---
   return(INIT_SUCCEEDED);
}

//+------------------------------------------------------------------+
//| Expert deinitialization function                                 |
//+------------------------------------------------------------------+
void OnDeinit(const int reason) 
{
//--- destroy timer
   EventKillTimer();
   
}

//+------------------------------------------------------------------+
//| Expert tick function                                             |
//+------------------------------------------------------------------+
void OnTick() 
{
    
}

//+------------------------------------------------------------------+
//| Timer function                                                   |
//+------------------------------------------------------------------+
void OnTimer() 
{

}
 
//+------------------------------------------------------------------+
//| Trade function                                                   |
//+------------------------------------------------------------------+
void OnTrade() 
{

}
 
//+------------------------------------------------------------------+
//| TradeTransaction function                                        |
//+------------------------------------------------------------------+
void OnTradeTransaction(const MqlTradeTransaction& trans,
                        const MqlTradeRequest& request,
                        const MqlTradeResult& result) 
{

}
 
//+------------------------------------------------------------------+
//| Tester function                                                  |
//+------------------------------------------------------------------+
double OnTester() 
{
   double ret=0.0;

   return(ret);
}
 
//+------------------------------------------------------------------+ Stop barra a barra




/*

   //anotações
            
 //Stop barra a barra
 //Estrutura de repetição "for"
 for (int i = PositionsTotal(); i>=0; i--){         //cataloga todas as operações aberta
    if (PositionGetSymbol (i) ==_symbol) {          //filtra pelo ativo atual
        if (PositionGetInteger(POSTION_TYPE) == POSTION_TYPE_BUY){           // filtra operações de compra
            //MOVER STOP PARA MINIMA DA PROXIMA barra    
            if (contarCandle > barraOperacao){
                double StopLoss =NoramlizaPreco(iLow(_Symbol, PERIOD_M15, 1));
                DayTrade.PositionModify(_Symbol, StopLoss, 0);
            }
        }
        if (PositionGetInteger(POSTION_TYPE) == POSTION_TYPE_SELL){           // filtra operações de VENDA
            //MOVER STOP PARA MINIMA DA PROXIMA barra    
            if (contarCandle > barraOperacao){
                double StopLoss =NoramlizaPreco(iLow(_Symbol, PERIOD_M15, 1));
                DayTrade.PositionModify(_Symbol, StopLoss, 0);
            }
        }
    }
}

// LOGICA DE CONTAR TEMPO
//NÃO DEIXAR ROBOZINHO FAZER MAIS QUE UMA OPERAÇÃO POR CANDLE


*/

