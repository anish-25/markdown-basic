# TerraPay APIs

This section describes the TerraPay API suite available for integration by send partners. These APIs allow send partners to use the services offered by TerraPay as described above. Before getting into the API details, the following section describes in brief the steps that are to be performed to execute a remittance transaction.


Basic Transaction Steps

* Sender initiates a transaction from ,
   * A registered Mobile Wallet
   * An active Bank Account
   * At a MTO agent
* The sender provides the beneficiary mobile number that will receive the funds for remittances to mobile wallet.
* The sender provides the beneficiary bank account details that will receive funds for remittances to bank accounts.
* Sending partner forwards the beneficiary mobile number/bank account to TerraPay to validate if the beneficiary can receive funds.
* TerraPay validates if the beneficiary mobile number is associated with a valid payment instrument and if that instrument is active and can receive funds for remittances to mobile wallets.
* TerraPay validates if the bank is supported and the banking details provided are correct for remittances to bank accounts.
* In addition where ever the receiving partner can provide the beneficiary name, TerraPay does name matching using a propriety fuzzy logic algorithm.
* If the validation is successful then the sender proceeds to the next step which is to initiate a quote request.
* Sender provides the amount to be transferred. TerraPay will process the quote and provide the sender with the foreign exchange rate and the amount the beneficiary will receive.
* Sender then confirms the transaction.
* TerraPay validates the transaction and sends a request to the receiving partner to credit the amount to beneficiary mobile number or bank account.


<aside class="notice">
**NOTE- Both sender and beneficiary KYC has to be provided by the sending and receiving partners to TerraPay in order to perform sanctions screening and AML/CFT validations. This information is mandatory and has to be provided via the API calls.
</aside>
**NOTE**:
All API calls to the TerraPay Network should include the following HTTP Headers

`X-USERNAME: "partnerUserName"`

`X-PASSWORD: "partnerPassWord"`

`X-DATE: "YYYY-MM-DD HH:mm:ss"`

`X-ORIGINCOUNTRY: "Country Code in which the transaction is created. ISO Alpha 2 standard"`

X-USERNAME, X-PASSWORD values will be shared with the Partner during the on boarding process on test and production environments separately.
Username and Password is always case-insensitive.

X-PASSWORD must be SHA256 hash encoded when sent over the API request.