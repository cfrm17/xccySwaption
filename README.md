# CROSS CURRENCY EUROPEAN SWAPTION Valuation


A Cross Currency European Swaption is a European Swaption to enter into a swap to exchange cash flows in two different currencies. The domestic and foreign swap leg cash flows can be fixed or floating. The model outlined here is called a Multi-Currency Terminal Swap Rate Model which generalizes a Terminal Swap Rate Model to incorporate foreign exchange. The main idea behind a Terminal Swap Rate Model is to assume that the discount factors at the option maturity can be written as a function of the underlying swap rates. This assumption reduces the number of stochastic variables that need to be modelled.    

A Cross Currency European Swaption gives the holder the option to enter into a swap to exchange cash flows in two different currencies. The domestic and foreign swap leg cash flows can be fixed or floating. The cash flow generation can be referred to as https://finpricing.com/lib/FiBondCoupon.html

The underlying cross-currency swap can be fixed-to-fixed, fixed-to-floating and floating-to-floating types with possible floating spread and principal exchanges which may happen at the beginning of the swap or at the end of the swap or at both the beginning and the end. The floating index interest rate for the CAD is BA rate and the one for USD is the LIBOR rate. In this swaption, the BA-LIBOR basis spread is also considered.

Even for a European cross-currency swaptions, a number of enforced assumptions have to be introduced to reduce the complexity of the problem. Some of the assumptions are purely technical and some of them are supported by historical observations. One of the technical assumptions is that PVBPs for both currencies at a swaption maturity can be approximated by the corresponding forward PVBPs.

Let   be integers and

 		 

Let the domestic and foreign daycount fractions be defined, respectively, as

    ,    ,       ,    ,   

and  ,  be the domestic and foreign forward interest rates seen at time   for the forward accrual periods of  ,  ,  ,  . We define  ,   as the domestic and foreign discount factors at   to the time points  , , respectively.

Let the present values, at time , of the domestic and foreign fixed leg cash flows be respectively defined as

 		(1a) 

 	(1b)

 

 
  are the domestic and foreign notionals, respectively.
 	are the domestic and foreign fixed rates, respectively.
  is the FX rate at time T expressed as units of domestic per unit of foreign currency.
 if notional amounts are exchanged at the maturity of the swap, else 
  if notional amounts are exchanged at the start of the swap, else  


Let the present values, at time , of the domestic and foreign floating leg cash flows be respectively defined as

 	(1c)

											(1d)
 

 	

 				
 are the domestic and foreign floating rate spreads, respectively.

We define the domestic and foreign PVBP factors, respectively, as.

    		  ,      		(2)

and the domestic and foreign vanilla swap rates, respectively, as.

 		  ,  		(3)

With (2) and (3) we can re-express 1(a,b,c,d) at time  , assuming  , as:

 				(4a)

 			(4b)

 			(4c)

 			(4d)

Note: that we have also added a basis spread,  , to the domestic swap rate.

Further simplifying we have

 		 		(5a)
						 
 

 	 			(5b)
						 

 	 				(5c)
        						 
						 

 	 			(5d)
 



We represent the present values, at time  , of a swap to exchange the domestic and foreign leg cash flows as

 						(6a)
 						(6b)
 						(6c)
 						(6d) 

where,   indicates a pay-foreign swap and   indicates a receive-foreign swap. 
Let  , then the payoff to the option at maturity can be expressed as:

 					(7a)
 					(7b)
 					(7c)
 					(7d)

We assume the following dynamics

 							(8)
 						(9)
 
 									(10)
 are deterministic functions of time.
  is a 4-dimensional Brownian motion.

Given the above dynamics the variables   are joint-normally distributed.

 									(11)

 				(12)
	
      							(13)

											
 							(14)


 					

  are forward values as seen from time  .

We calulate the time-t value of the options given in 7(a,b,c,d), where  , as
											

 			
            		(15a)
															
 
            		(15b)

											
 
            		(15c)


 
            		(15d)



Consider the following general form of the conditional expectation in 15(a,b,c,d)

 			(16)

 
 
 
 
		
 

 			(17)


  is the corresponding density function.

To solve (23) we condition first on  and   which yields
											
  
			 				(18)
				
 

 				(19)

 

 
 

 ,  are the corresponding conditional and trivariate densities.

Let
 		(20)

The  in  stands for Black-Scholes since depending on the signs of  and  , reduces to the Black-Scholes equation.

The evaluation of   is as follows:

Dropping the arguments of the functions  and   we write

 								(21)

Case 1: if  Then    	

Case 1a: if   then  
		Case 1b: if   then  

Case 2: if  Then  

		Case 2a: if  then  
		Case 2b: if   then  

Case 3: if  then  
		
		Case 3a: if   then  
Case 3b: if   

  

	
 
 
 

Refer to the Appendix  for details on calculating conditional moments of a multivariate normal distribution.


With  well defined we now need to solve
											
 		(22)

Let 

 	 	 			 			(23a,b,c)

Then

 	(24)

 is the multivariate normal density function.

We now proceed by conditioning on  and  to integrate with respect to  . Then we condition on  to integrate with respect to  . Then we integrate with respect to  . This allows us to write

 
 				(25)


We define the following

 	 	 			(26a,b,c)

 	 	 		(27a,b,c)

where, the bars on the variables above indicate that they are conditional moments.

We can now write

 
 				(28)


We make the following change of variables

 		 		 	(29a,b,c)

 			 			 		(30a,b,c)

(29a,b,c) &  (30a,b,c) imply

 		 		  	(31a,b,c)

Which allows us to express

 

 		(32)





