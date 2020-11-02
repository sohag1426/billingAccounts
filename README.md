# Billing Accounts

### Two main attributes of billing accounts are:
 * account_provider
   * Who holds the money and should pay to the account owner.
 
 * account_owner
   * Who owns the money in the account and will receive from account provider.
 
###  # Only account provider can cash out from the account.

###  # Each account must have proper Cash In and Cash Out transaction records.
###  # Account's Module removes operator_price in package table, operators_bills and operators_payments table.

### Dashboard Menu
* Accounts
  * Payable
  * Receivable
  
 ### Collection Distribution
 
 * Who is collecting money?
   * operator | Group Admin | Super Admin
   * If payment method is recharge or cash, the operator of the customer (Operator | Group Admin) is collecting money.
   * If Payment method is online, the merchant of the payment gateway (Operator | Group Admin | Super Admin) is collecting money.
 * How the customer's payment will be distributed among shareholders.
    * If payment Collector is operator
      * If Operator != Group Admin
      * Account Provider -> Operator
      * Account Owner -> Group Admin
      * Amount = collection * ((100-operator's share)/100)
      
      * Account Provider -> Group Admin
      * Account Owner -> Super Admin
      * Amount = collection * (Super Admin's Share/100)
      
    * If Payment Collector is Group Admin
      * If Group Admin != Operator
      * Account Provider -> Group Admin
      * Account Owner -> Operator
      * Amount = collection * (Operator's Share/100)
      
      * Account Provider -> Group Admin
      * Account Owner -> Super Admin
      * Amount = collection * (Super Admin's Share/100)
      
    * If Payment Collector is Super Admin
      * Account Provider -> Super Admin
      * Account Owner -> Group Admin
      * Amount = collection * ((100-Super Admin's Share)/100)
      
      * If Group Admin != Operator
      * Account Provider -> Group Admin
      * Account Owner -> Operator
      * Amount = collection * (Operator's Share/100)
