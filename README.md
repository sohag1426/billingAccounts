# Billing Accounts

### Two main attributes of billing accounts are:
 * account_provider
   * Who holds the money and should pay to the account owner.
 
 * account_owner
   * Who owns the money in the account and will receive from account provider.
 
###  # Account provider will send money to account owner.

###  # Account owner needs to receive money sent by the account provider to complete the transaction.

###  # Each account must have proper Cash In and Cash Out transaction records.

### Dashboard Menu
* Accounts
  * Payable
  * Receivable
  
 ### Collection Distribution
 * The Amount Distributed among the shareholder's is not the income of the shareholder's. The amount Cash out for the operator is the income of the operator.
 * Who is collecting money?
   * operator | Group Admin | Super Admin
   * If payment method is recharge or cash, the operator of the customer (Operator | Group Admin) is collecting money.
   * If Payment method is online, the merchant of the payment gateway (Operator | Group Admin | Super Admin) is collecting money.
 * How the customer's payment will be distributed among shareholders.
    * If payment Collector is operator(role)
      * Account Provider -> Operator
      * Account Owner -> Group Admin
      * Amount = collection * ((100-operator's share)/100)
      
      * Account Provider -> Group Admin
      * Account Owner -> Super Admin
      * Amount = collection * (Super Admin's Share/100)
      
    * If Payment Collector is Group Admin (role)
      * If Group Admin != Operator
      * Account Provider -> Group Admin
      * Account Owner -> Operator
      * Amount = collection * (Operator's Share/100)
      
      * Account Provider -> Group Admin
      * Account Owner -> Super Admin
      * Amount = collection * (Super Admin's Share/100)
      
    * If Payment Collector is Super Admin (role)
      * Account Provider -> Super Admin
      * Account Owner -> Group Admin
      * Amount = collection * ((100-Super Admin's Share)/100)
      
      * If Group Admin != Operator
      * Account Provider -> Group Admin
      * Account Owner -> Operator
      * Amount = collection * (Operator's Share/100)
