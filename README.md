# MBS Model

This article presents a Mortgage-Backed Security (MBS) model. Our analysis has focused on the model’s theoretical underpinnings and its implementation. We have found that the theoretical assumptions with respect to the prepayment model are suitable for trading purposes. 

We begin with a review of mortgage mathematics and outlines variables that are used in subsequent sections.  Payment schedules of mortgages and the cashflows accruing to an MBS holder are also discussed in this section. A discounted cash flow (DCF) model constitutes the main pricing engine of the MBS, however, the main theoretical aspects of the model pertain to the prepayment assumptions corresponding to the underlying mortgage. A discussion of the two prepayment models is outlined in the next section.

Standard Canadian balloon mortgages consist of fixed level monthly payments with a semi-annually compounded rate. This requires that the annual MBS coupon rate (see https://finpricing.com/lib/FiBondCoupon.html) and the annual weighted average mortgage rate be converted as:


To price an MBS we need to evaluate the monthly payments made to the underlying mortgage. These payments are divided into scheduled and unscheduled payments. The scheduled payments consist of principle and interest payments and the unscheduled payments consist solely of principle prepayments.

The scheduled monthly payment is calculated where,

c  = remaining average amortization at time of pricing.
r = weighted average mortgage coupon, expressed on a monthly basis.

Given the monthly payment the share of interest and principle payments are determined. The scheduled remaining principles is provide.

Unscheduled payments are classed as partial prepayments or outright liquidation. Under a typical mortgage contract partial prepayments are allowed each month up to a maximum percentage of the original borrowed principle. While outright liquidations occur when the mortgage is prepaid in full usually due to personal circumstances of the borrower necessitating the sale of the property. Examples would include death, divorce, and change of residence. Liquidations can also occur if mortgage rates fall by a sufficient amount below the contract rate after taking into account refinancing costs.

Liquidation Rates (LQR) and Partial Prepayment Rates (PPR) are quoted as annualized rates and are calculated from their corresponding monthly rates.

Monthly liquidation and partial prepayment rates, denoted q and p, are treated as primary inputs and can be estimated from historical data. A brief digression on different estimation methods will be presented below.

Given estimates of the liquidation and prepayment rates the estimated monthly payments are calculated  

Provided there are a reasonable number of mortgages left in the pool liquidations do not substantially affect the amortization of the security. Implying that the monthly payment will be lower in proportion to the remaining mortgages after liquidation. That proportion being   in the kth month. Partial prepayments on the other hand will not affect the monthly payment but will reduce the term and amortization of the mortgage.


As above the estimate of the scheduled remaining principal balance is calculated where r is	monthly weighted average mortgage rate

The estimated remaining principal balance can be determined reflecting both liquidation and partial prepayments as:




