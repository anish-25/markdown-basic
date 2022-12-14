#  Create a Business Transaction
This API is used to create business transaction. This is similar to create a transaction with additional parameters required to conduct business transaction. Business transactions can be as follows:

* Business to Business (B2B)
* Business to Person (B2P)
* Person to Business (P2B)

**The URI format is:**/transactions

 
## B2B transaction to a Bank 
### B2B transaction to a Bank <a class="tryitbutton" href='https://developers.terrapay.com/try-it/b2b-transaction-bank' target="_blank">Try it </a>

> B2B transcation to a bank

```shell
curl --location --request POST  'https://uat-connect.terrapay.com:21211/eig/gsma/transactions'\
--header 'X-USERNAME:terrapayuser '\
--header 'X-PASSWORD: 101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b'\
--header 'X-DATE: 2018-03-12 09:00:00'\
--header 'X-ORIGINCOUNTRY:FR'\
--header 'Content-Type: application/json'\
--data--raw
{
	"currency": "NGN",
	"type": "b2b",
	"requestDate": "2020-01-02 10:51:16",
	"amount": "35500.00",
	"descriptionText": "Gift for my brother",
	"requestingOrganisationTransactionReference": "12345868378400387540",
	"sendingAmount": "35500.00",
	"payinCcyCode": "USD",
	"provider": "23401",
	"paymentMode": "cash",
	"authenticationPartnerCode": "4534",
	"paymentOption": "Mobile Wallet",
	"sendingPartnerCode": "343432223",
	"receivingPartnerCode": "343432223",
	"debitParty": [
	{
		"key": "msisdn",
		"value": "+4491509874561"
	} 
	],
		"creditParty": [
	{
		"key": "bankaccountno",
		"value": "1976010126"
	},
	{
		"key": "sortcode",
		"value": "CITINGLA"
	},
	{
		"key": "organisationid",
		"value": "Citi Bank"
	},
	{
		"key": "banksubcode",
		"value": "0001"
	},
	{
		"key": "bankBranchName",
		"value": "Citi Bank"
	},
	{
		"key": "accountName",
		"value": "Rajesh"
	},
	{
		"key": "accountIBAN",
		"value": "GB29NWBK60161331926819"
	},
	{
		"key": "accountAdditionalNo1",
		"value": "2656915085434"
	}
	],
		"senderKyc": {

	},
		"recipientKyc": {

	},
		"internationalTransferInformation": {
			"quoteId": "QT0FEO4OZZ28PLCA5",
			"receivingCountry": "NG",
			"remittancePurpose": "Advanced Goods Payments",
			"sourceOfFunds": "Savings"
	},
	"business": {
		"senderKyc": {
			"businessName": "sample business",
			"businessAddress1": "walton's road",
			"businessAddressCity": "Lyon",
			"businessAddressCountryCode": "US",
			"businessPrimaryContactCountryCode": "US",
			"businessPrimaryContactNo": "3472034605",
			"businessDescription": "Electronics",
			"businessCountryCode": "US",
			"businessRegistrationType": "b2b",
			"businessRegistrationNumber": "23123456789",
			"businessRegistrationIssueDate": "2020-09-26",
			"businessIDValidThru": "2033-09-26"
		},
		"recepientKyc": {
			"businessName": "oyugi randy",
			"businessPINCode": "123456",
			"businessAddress1": "24",
			"businessAddress2": "walton's road",
			"businessAddressCity": "newyork",
			"businessAddressState": "NYC",
			"businessAddressCountryCode": "NG",
			"businessAddressZip": "123456",
			"businessPrimaryContactCountryCode": "NG",
			"businessPrimaryContactNo": "232323212",
			"businessPrimaryContactNoType": "Mobile",
			"businessDescription": "Electronics wholesale",
			"businessEmail": "rs.electronics@gmail.com",
			"businessCountryCode": "NG",
			"businessRegistrationType": "b2b",
			"businessRegistrationNumber": "2312345678912",
			"businessRegistrationIssuedBy": "NYC_TRADE",
			"businessRegistrationIssuedAt": "NYC",
			"businessRegistrationIssueDate": "2002-08-26",
			"businessIDValidThru": "2036-09-26",
			"typeofbusiness": "Electronics",
			"businessPObox": "12345",
			"businessMobile": "343234433"
		}
	}	
}
		
```
```javascript
var myHeaders = new Headers();
myHeaders.append("X-USERNAME", "terrapayuser");
myHeaders.append("X-PASSWORD", "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b");
myHeaders.append("X-DATE", "2018-04-04 09:27:16");
myHeaders.append("X-ORIGINCOUNTRY", "US");
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "amount": "500",
  "currency": "INR",
  "type": "b2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId004",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA1XDKDL53E",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://uat-connect.terrapay.com:21211/eig/gsma/transactions", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
```python
import requests
import json

url = "https://uat-connect.terrapay.com:21211/eig/gsma/transactions"

payload = json.dumps({
  "amount": "500",
  "currency": "INR",
  "type": "b2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId004",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA1XDKDL53E",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})
headers = {
  'X-USERNAME': 'terrapayuser',
  'X-PASSWORD': '101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b',
  'X-DATE': '2018-04-04 09:27:16',
  'X-ORIGINCOUNTRY': 'US',
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```
```java
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"amount\": \"500\",\r\n    \"currency\": \"INR\",\r\n    \"type\": \"b2b\",\r\n    \"descriptionText\": \"Gift for my brother\",\r\n    \"requestDate\": \"2021-05-23 08:19:36\",\r\n    \"requestingOrganisationTransactionReference\": \"SrcTxnId004\",\r\n    \"debitParty\": [\r\n        {\r\n            \"key\": \"msisdn\",\r\n            \"value\": \"+971810456234\"\r\n        }\r\n    ],\r\n    \"creditParty\": [\r\n        {\r\n            \"key\": \"bankaccountno\",\r\n            \"value\": \"50100002965304\"\r\n        },\r\n        {\r\n            \"key\": \"organisationid\",\r\n            \"value\": \"HDFC Bank\"\r\n        },\r\n        {\r\n            \"key\": \"sortcode\",\r\n            \"value\": \"HDFC0001626\"\r\n        }\r\n    ],\r\n    \"senderKyc\": {},\r\n    \"recipientKyc\": {},\r\n    \"sendingAmount\": \"35500.00\",\r\n    \"payinCcyCode\": \"USD\",\r\n    \"paymentMode\": \"cash\",\r\n    \"authenticationPartnerCode\": \"4534\",\r\n    \"paymentOption\": \"Mobile Wallet\",\r\n    \"sendingPartnerCode\": \"343432223\",\r\n    \"receivingPartnerCode\": \"343432223\",\r\n    \"business\": {\r\n        \"senderKyc\": {\r\n            \"businessName\": \"sample business\",\r\n            \"businessAddress1\": \"alton's road\",\r\n            \"businessAddressCity\": \"Lyon\",\r\n            \"businessAddressCountryCode\": \"US\",\r\n            \"businessPrimaryContactCountryCode\": \"US\",\r\n            \"businessPrimaryContactNo\": \"3472034605\",\r\n            \"businessDescription\": \"Electronics\",\r\n            \"businessCountryCode\": \"US\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"23123456789\",\r\n            \"businessRegistrationIssueDate\": \"2001-09-26\",\r\n            \"businessIDValidThru\": \"2033-09-26\",\r\n            \"businessEmail\": \"test@testemail.com\"\r\n        },\r\n        \"recepientKyc\": {\r\n            \"businessName\": \"Oyugi Randy Electric Sale Pvt. Ltd.\",\r\n            \"businessPINCode\": \"123456\",\r\n            \"businessAddress1\": \"24\",\r\n            \"businessAddress2\": \"walton's road\",\r\n            \"businessAddressCity\": \"newyork\",\r\n            \"businessAddressState\": \"NYC\",\r\n            \"businessAddressCountryCode\": \"NG\",\r\n            \"businessAddressZip\": \"123456\",\r\n            \"businessPrimaryContactCountryCode\": \"NG\",\r\n            \"businessPrimaryContactNo\": \"232323212\",\r\n            \"businessPrimaryContactNoType\": \"Mobile\",\r\n            \"businessDescription\": \"Electronics wholesale\",\r\n            \"businessEmail\": \"rs.electronics@gmail.com\",\r\n            \"businessCountryCode\": \"NG\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"2312345678912\",\r\n            \"businessRegistrationIssuedBy\": \"NYC_TRADE\",\r\n            \"businessRegistrationIssuedAt\": \"NYC\",\r\n            \"businessRegistrationIssueDate\": \"2002-08-26\",\r\n            \"businessIDValidThru\": \"2036-09-26\",\r\n            \"typeofbusiness\": \"Electronics\",\r\n            \"businessPObox\": \"12345\",\r\n            \"businessMobile\": \"343234433\"\r\n        }\r\n    },\r\n    \"internationalTransferInformation\": {\r\n        \"quoteId\": \"QR037C1NA1XDKDL53E\",\r\n        \"receivingCountry\": \"IN\",\r\n        \"remittancePurpose\": \"Business Travel\",\r\n        \"sourceOfFunds\": \"Business Income\",\r\n        \"relationshipSender\": \"Employer\"\r\n    }\r\n}");
Request request = new Request.Builder()
  .url("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")
  .method("POST", body)
  .addHeader("X-USERNAME", "terrapayuser")
  .addHeader("X-PASSWORD", "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b")
  .addHeader("X-DATE", "2018-04-04 09:27:16")
  .addHeader("X-ORIGINCOUNTRY", "US")
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();
```
```ruby
require "uri"
require "json"
require "net/http"

url = URI("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")

https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true

request = Net::HTTP::Post.new(url)
request["X-USERNAME"] = "terrapayuser"
request["X-PASSWORD"] = "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b"
request["X-DATE"] = "2018-04-04 09:27:16"
request["X-ORIGINCOUNTRY"] = "US"
request["Content-Type"] = "application/json"
request.body = JSON.dump({
  "amount": "500",
  "currency": "INR",
  "type": "b2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId004",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA1XDKDL53E",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})

response = https.request(request)
puts response.read_body

```
### URL
https://uat-connect.terrapay.com:21211/eig/gsma/transactions
### HTTP Request

`POST /eig/gsma/transactions HTTP/1.1 `


## B2B transaction to mobile wallet 
### B2B transaction to mobile wallet <a class="tryitbutton" href='https://developers.terrapay.com/try-it/b2b-transaction-mobile' target="_blank">Try it </a>

> B2B transaction to mobile wallet

```shell
curl --location --request POST 'https://uat-connect.terrapay.com:21211/eig/gsma/transactions'\
--header 'X-USERNAME: terrapayuser'\
--header 'X-PASSWORD:101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b'\
--header 'X-DATE: 2017-05-03 11:00:00'\
--header 'X-ORIGINCOUNTRY:US'\
--header 'Content-Type: application/json'\
--data--raw
{
	"currency": "NGN",
	"type": "b2b",
	"requestDate": "2020-01-02 10:51:16",
	"amount": "35500.00",
	"descriptionText": "Gift for my brother",
	"requestingOrganisationTransactionReference": "12345868378400387540",
	"sendingAmount": "35500.00",
	"payinCcyCode": "USD",
	"provider": "23401",
	"paymentMode": "cash",
	"authenticationPartnerCode": "4534",
	"paymentOption": "Mobile Wallet",
	"sendingPartnerCode": "343432223",
	"receivingPartnerCode": "343432223",
	"debitParty": [
	{
		"key": "msisdn",
		"value": "+4491509874561"
	} 
	],
		"creditParty": [
	{
		"key": "msisdn",
		"value": "+2349061114853"
	}
	],
		"senderKyc": {

	},
		"recipientKyc": {
	},
		"internationalTransferInformation": {
			"quoteId": "QT0FEO4OZZ28PLCA5",
			"receivingCountry": "NG",
			"remittancePurpose": "Advanced Goods Payments",
			"sourceOfFunds": "Savings"
	},
	"business": {
		"senderKyc": {
			"businessName": "sample business",
			"businessAddress1": "walton's road",
			"businessAddressCity": "Lyon",
			"businessAddressCountryCode": "US",
			"businessPrimaryContactCountryCode": "US",
			"businessPrimaryContactNo": "3472034605",
			"businessDescription": "Electronics",
			"businessCountryCode": "US",
			"businessRegistrationType": "b2b",
			"businessRegistrationNumber": "23123456789",
			"businessRegistrationIssueDate": "2020-09-26",
			"businessIDValidThru": "2033-09-26"
		},
		"recepientKyc": {
			"businessName": "oyugi randy",
			"businessPINCode": "123456",
			"businessAddress1": "24",
			"businessAddress2": "walton's road",
			"businessAddressCity": "newyork",
			"businessAddressState": "NYC",
			"businessAddressCountryCode": "NG",
			"businessAddressZip": "123456",
			"businessPrimaryContactCountryCode": "NG",
			"businessPrimaryContactNo": "232323212",
			"businessPrimaryContactNoType": "Mobile",
			"businessDescription": "Electronics wholesale",
			"businessEmail": "rs.electronics@gmail.com",
			"businessCountryCode": "NG",
			"businessRegistrationType": "b2b",
			"businessRegistrationNumber": "2312345678912",
			"businessRegistrationIssuedBy": "NYC_TRADE",
			"businessRegistrationIssuedAt": "NYC",
			"businessRegistrationIssueDate": "2002-08-26",
			"businessIDValidThru": "2036-09-26",
			"typeofbusiness": "Electronics",
			"businessPObox": "12345",
			"businessMobile": "343234432"
		}
	}	
}

```
```javascript
var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "amount": "500",
  "currency": "INR",
  "type": "b2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId004",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA1XDKDL53E",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://uat-connect.terrapay.com:21211/eig/gsma/transactions", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
```python
import requests
import json

url = "https://uat-connect.terrapay.com:21211/eig/gsma/transactions"

payload = json.dumps({
  "amount": "500",
  "currency": "INR",
  "type": "b2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId004",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA1XDKDL53E",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```
```java
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"amount\": \"500\",\r\n    \"currency\": \"INR\",\r\n    \"type\": \"b2b\",\r\n    \"descriptionText\": \"Gift for my brother\",\r\n    \"requestDate\": \"2021-05-23 08:19:36\",\r\n    \"requestingOrganisationTransactionReference\": \"SrcTxnId004\",\r\n    \"debitParty\": [\r\n        {\r\n\t\t\"key\": \"msisdn\",\r\n\t\t\"value\": \"+4491509874561\"\r\n\t}\r\n    ],\r\n    \"creditParty\": [\r\n        {\r\n\t\t\"key\": \"msisdn\",\r\n\t\t\"value\": \"+2349061114853\"\r\n\t}\r\n    ],\r\n    \"senderKyc\": {},\r\n    \"recipientKyc\": {},\r\n    \"sendingAmount\": \"35500.00\",\r\n    \"payinCcyCode\": \"USD\",\r\n    \"paymentMode\": \"cash\",\r\n    \"authenticationPartnerCode\": \"4534\",\r\n    \"paymentOption\": \"Mobile Wallet\",\r\n    \"sendingPartnerCode\": \"343432223\",\r\n    \"receivingPartnerCode\": \"343432223\",\r\n    \"business\": {\r\n        \"senderKyc\": {\r\n            \"businessName\": \"sample business\",\r\n            \"businessAddress1\": \"alton's road\",\r\n            \"businessAddressCity\": \"Lyon\",\r\n            \"businessAddressCountryCode\": \"US\",\r\n            \"businessPrimaryContactCountryCode\": \"US\",\r\n            \"businessPrimaryContactNo\": \"3472034605\",\r\n            \"businessDescription\": \"Electronics\",\r\n            \"businessCountryCode\": \"US\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"23123456789\",\r\n            \"businessRegistrationIssueDate\": \"2001-09-26\",\r\n            \"businessIDValidThru\": \"2033-09-26\",\r\n            \"businessEmail\": \"test@testemail.com\"\r\n        },\r\n        \"recepientKyc\": {\r\n            \"businessName\": \"Oyugi Randy Electric Sale Pvt. Ltd.\",\r\n            \"businessPINCode\": \"123456\",\r\n            \"businessAddress1\": \"24\",\r\n            \"businessAddress2\": \"walton's road\",\r\n            \"businessAddressCity\": \"newyork\",\r\n            \"businessAddressState\": \"NYC\",\r\n            \"businessAddressCountryCode\": \"NG\",\r\n            \"businessAddressZip\": \"123456\",\r\n            \"businessPrimaryContactCountryCode\": \"NG\",\r\n            \"businessPrimaryContactNo\": \"232323212\",\r\n            \"businessPrimaryContactNoType\": \"Mobile\",\r\n            \"businessDescription\": \"Electronics wholesale\",\r\n            \"businessEmail\": \"rs.electronics@gmail.com\",\r\n            \"businessCountryCode\": \"NG\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"2312345678912\",\r\n            \"businessRegistrationIssuedBy\": \"NYC_TRADE\",\r\n            \"businessRegistrationIssuedAt\": \"NYC\",\r\n            \"businessRegistrationIssueDate\": \"2002-08-26\",\r\n            \"businessIDValidThru\": \"2036-09-26\",\r\n            \"typeofbusiness\": \"Electronics\",\r\n            \"businessPObox\": \"12345\",\r\n            \"businessMobile\": \"343234433\"\r\n        }\r\n    },\r\n    \"internationalTransferInformation\": {\r\n        \"quoteId\": \"QR037C1NA1XDKDL53E\",\r\n        \"receivingCountry\": \"IN\",\r\n        \"remittancePurpose\": \"Business Travel\",\r\n        \"sourceOfFunds\": \"Business Income\",\r\n        \"relationshipSender\": \"Employer\"\r\n    }\r\n}");
Request request = new Request.Builder()
  .url("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();
```
```ruby
require "uri"
require "json"
require "net/http"

url = URI("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")

https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true

request = Net::HTTP::Post.new(url)
request["Content-Type"] = "application/json"
request.body = JSON.dump({
  "amount": "500",
  "currency": "INR",
  "type": "b2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId004",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA1XDKDL53E",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})

response = https.request(request)
puts response.read_body

```
### URL
https://uat-connect.terrapay.com:21211/eig/gsma/transactions
### HTTP Request
`POST /eig/gsma/transactions HTTP/1.1 `


## B2P transaction to bank 
### B2P transaction to bank <a class="tryitbutton" href='https://developers.terrapay.com/try-it/b2p-transaction-bank' target="_blank">Try it </a>

> B2P transaction to bank

```shell
curl --location --request POST 'https://uat-connect.terrapay.com:21211/eig/gsma/transactions'\
--header 'X-USERNAME:terrapayuser'\
--header 'X-PASSWORD: 101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b'\
--header 'X-DATE: 2017-05-03 11:00:00'\
--header 'X-ORIGINCOUNTRY:FR'\
--header 'Content-Type: application/json'\
--data--raw
{
	"currency": "NGN",
	"type": "b2p",
	"requestDate": "2020-01-02 10:51:16",
	"amount": "35500.00",
	"descriptionText": "Gift for my brother",
	"requestingOrganisationTransactionReference": "123458w8378400387553",
	"sendingAmount": "35500.00",
	"payinCcyCode": "USD",
	"provider": "23401",
	"paymentMode": "cash",
	"authenticationPartnerCode": "4534",
	"paymentOption": "Mobile Wallet",
	"sendingPartnerCode": "343432223",
	"receivingPartnerCode": "343432223",
	"debitParty": [
	{
		"key": "msisdn",
		"value": "+4491509874561"
	} 
	],
		"creditParty": [
	{
		"key": "bankaccountno",
		"value": "1976010126"
	},
	{
		"key": "sortcode",
		"value": "CITINGLA"
	},
	{
		"key": "organisationid",
		"value": "Citi Bank"
	},
	{
		"key": "banksubcode",
		"value": "0001"
	},
	{
		"key": "bankBranchName",
		"value": "Citi Bank"
	},
	{
		"key": "accountName",
		"value": "Rajesh"
	},
	{
		"key": "accountIBAN",
		"value": "GB29NWBK60161331926819"
	},
	{
		"key": "accountAdditionalNo1",
		"value": "2656915085434"
	}
	],
		"senderKyc": {
			
	},
	"recipientKyc":{
		"primaryContactCountryCode": "NG",
		"primaryContactNo": "2349061114853",
		"primaryContactNoType": "personal",
		"subjectName":{
			"firstName": "oyugi",
			"lastName": "randy",
			"fullName": "oyugi randy"
		}
	},
   		"internationalTransferInformation":{
			"quoteId": "QT0FEO4UG99LQNQC3",
			"receivingCountry": "NG",
			"remittancePurpose": "Business Travel",
			"sourceOfFunds": "Business Income",
			"relationshipSender": "Employer"
	},
	"business": {
		"senderKyc": {
			"businessName": "sample business",
			"businessAddress1": "alton's road",
			"businessAddressCity": "Lyon",
			"businessAddressCountryCode": "US",
			"businessPrimaryContactCountryCode": "US",
			"businessPrimaryContactNo": "3472034605",
			"businessDescription": "Electronics",
			"businessCountryCode": "US",
			"businessRegistrationType": "b2p",
			"businessRegistrationNumber": "23123456789",
			"businessRegistrationIssueDate": "2001-09-26",
			"businessIDValidThru": "2033-09-26"
		},
		"recepientKyc": {

 		}
	}
}

```
```javascript
var myHeaders = new Headers();
myHeaders.append("X-USERNAME", "terrapayuser");
myHeaders.append("X-PASSWORD", "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b");
myHeaders.append("X-DATE", "2018-04-04 09:27:16");
myHeaders.append("X-ORIGINCOUNTRY", "US");
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "amount": "500",
  "currency": "INR",
  "type": "b2p",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId003",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {
    "subjectName": {
      "firstName": "Deepa",
      "lastName": "Jain",
      "fullName": "Deepa Jain"
    }
  },
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {}
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NZWQLJ42P1F",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://uat-connect.terrapay.com:21211/eig/gsma/transactions", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
```python
import requests
import json

url = "https://uat-connect.terrapay.com:21211/eig/gsma/transactions"

payload = json.dumps({
  "amount": "500",
  "currency": "INR",
  "type": "b2p",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId003",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {
    "subjectName": {
      "firstName": "Deepa",
      "lastName": "Jain",
      "fullName": "Deepa Jain"
    }
  },
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {}
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NZWQLJ42P1F",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})
headers = {
  'X-USERNAME': 'terrapayuser',
  'X-PASSWORD': '101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b',
  'X-DATE': '2018-04-04 09:27:16',
  'X-ORIGINCOUNTRY': 'US',
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```
```java
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"amount\": \"500\",\r\n    \"currency\": \"INR\",\r\n    \"type\": \"b2p\",\r\n    \"descriptionText\": \"Gift for my brother\",\r\n    \"requestDate\": \"2021-05-23 08:19:36\",\r\n    \"requestingOrganisationTransactionReference\": \"SrcTxnId003\",\r\n    \"debitParty\": [\r\n        {\r\n            \"key\": \"msisdn\",\r\n            \"value\": \"+971810456234\"\r\n        }\r\n    ],\r\n    \"creditParty\": [\r\n        {\r\n            \"key\": \"bankaccountno\",\r\n            \"value\": \"50100002965304\"\r\n        },\r\n        {\r\n            \"key\": \"organisationid\",\r\n            \"value\": \"HDFC Bank\"\r\n        },\r\n        {\r\n            \"key\": \"sortcode\",\r\n            \"value\": \"HDFC0001626\"\r\n        }\r\n    ],\r\n    \"senderKyc\": {},\r\n    \"recipientKyc\": {\r\n        \"subjectName\": {\r\n            \"firstName\": \"Deepa\",\r\n            \"lastName\": \"Jain\",\r\n            \"fullName\": \"Deepa Jain\"\r\n        }\r\n    },\r\n    \"sendingAmount\": \"35500.00\",\r\n    \"payinCcyCode\": \"USD\",\r\n    \"paymentMode\": \"cash\",\r\n    \"authenticationPartnerCode\": \"4534\",\r\n    \"paymentOption\": \"Mobile Wallet\",\r\n    \"sendingPartnerCode\": \"343432223\",\r\n    \"receivingPartnerCode\": \"343432223\",\r\n    \"business\": {\r\n        \"senderKyc\": {\r\n            \"businessName\": \"sample business\",\r\n            \"businessAddress1\": \"alton's road\",\r\n            \"businessAddressCity\": \"Lyon\",\r\n            \"businessAddressCountryCode\": \"US\",\r\n            \"businessPrimaryContactCountryCode\": \"US\",\r\n            \"businessPrimaryContactNo\": \"3472034605\",\r\n            \"businessDescription\": \"Electronics\",\r\n            \"businessCountryCode\": \"US\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"23123456789\",\r\n            \"businessRegistrationIssueDate\": \"2001-09-26\",\r\n            \"businessIDValidThru\": \"2033-09-26\",\r\n            \"businessEmail\":\"test@testemail.com\"\r\n        },\r\n        \"recepientKyc\": {}\r\n    },\r\n    \"internationalTransferInformation\": {\r\n        \"quoteId\": \"QR037C1NZWQLJ42P1F\",\r\n        \"receivingCountry\": \"IN\",\r\n        \"remittancePurpose\": \"Business Travel\",\r\n        \"sourceOfFunds\": \"Business Income\",\r\n        \"relationshipSender\": \"Employer\"\r\n    }\r\n}");
Request request = new Request.Builder()
  .url("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")
  .method("POST", body)
  .addHeader("X-USERNAME", "terrapayuser")
  .addHeader("X-PASSWORD", "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b")
  .addHeader("X-DATE", "2018-04-04 09:27:16")
  .addHeader("X-ORIGINCOUNTRY", "US")
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();
```
```ruby
require "uri"
require "json"
require "net/http"

url = URI("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")

https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true

request = Net::HTTP::Post.new(url)
request["X-USERNAME"] = "terrapayuser"
request["X-PASSWORD"] = "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b"
request["X-DATE"] = "2018-04-04 09:27:16"
request["X-ORIGINCOUNTRY"] = "US"
request["Content-Type"] = "application/json"
request.body = JSON.dump({
  "amount": "500",
  "currency": "INR",
  "type": "b2p",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId003",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {
    "subjectName": {
      "firstName": "Deepa",
      "lastName": "Jain",
      "fullName": "Deepa Jain"
    }
  },
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {}
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NZWQLJ42P1F",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})

response = https.request(request)
puts response.read_body

```
### URL
https://uat-connect.terrapay.com:21211/eig/gsma/transactions
### HTTP Request
`POST /eig/gsma/transactions HTTP/1.1 `

## B2P transaction to mobile wallet 
### B2P transaction to mobile wallet <a class="tryitbutton" href='https://developers.terrapay.com/try-it/b2p-transaction-mobile' target="_blank">Try it </a>


> B2P transaction to mobile wallet

```shell
curl --location --request POST 'https://uat-connect.terrapay.com:21211/eig/gsma/transactions'\
--header 'X-USERNAME: terrapayuser'\
--header 'X-PASSWORD: 101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b'\
--header 'X-DATE: 2019-08-25 12:00:00'\
--header 'X-ORIGINCOUNTRY:FR'\
--header 'Content-Type: application/json'\
--data-raw
{
	"currency": "NGN",
	"type": "b2p",
	"requestDate": "2020-01-02 10:51:16",
	"amount": "35500.00",
	"descriptionText": "Gift for my brother",
	"requestingOrganisationTransactionReference": "123458w8378400387553",
	"sendingAmount": "35500.00",
	"payinCcyCode": "USD",
	"provider": "23401",
	"paymentMode": "cash",
	"authenticationPartnerCode": "4534",
	"paymentOption": "Mobile Wallet",
	"sendingPartnerCode": "343432223",
	"receivingPartnerCode": "343432223",
	"debitParty": [
	{
		"key": "msisdn",
		"value": "+4491509874561"
	} 
	],
	"creditParty": [
		{
		"key": "msisdn",
		"value": "+2349061114853"
		}
	],
		"senderKyc": {
			
	},
	"recipientKyc":{
		"primaryContactCountryCode": "NG",
		"primaryContactNo": "2349061114853",
		"primaryContactNoType": "personal",
		"subjectName":{
			"firstName": "Kevin",
			"lastName": "Hawkins",
			"fullName": "Kevin Hawkins"
		}
	},
   		"internationalTransferInformation":{
			"quoteId": "QT0FEO4UG99LQNQC3",
			"receivingCountry": "NG",
			"remittancePurpose": "Business_Travel",
			"sourceOfFunds": "Business_Income",
			"relationshipSender": "Employer"
	},
	"business": {
		"senderKyc": {
			"businessName": "sample business",
			"businessAddress1": "alton's road",
			"businessAddressCity": "Lyon",
			"businessAddressCountryCode": "US",
			"businessPrimaryContactCountryCode": "US",
			"businessPrimaryContactNo": "3472034605",
			"businessDescription": "Electronics",
			"businessCountryCode": "US",
			"businessRegistrationType": "b2p",
			"businessRegistrationNumber": "23123456789",
			"businessRegistrationIssueDate": "2001-09-26",
			"businessIDValidThru": "2033-09-26"
		},
		"recepientKyc": {

 		}
	}
}

```
```javascript
var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "amount": "500",
  "currency": "INR",
  "type": "b2p",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId003",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {
    "subjectName": {
      "firstName": "Deepa",
      "lastName": "Jain",
      "fullName": "Deepa Jain"
    }
  },
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {}
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NZWQLJ42P1F",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://uat-connect.terrapay.com:21211/eig/gsma/transactions", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
```python
import requests
import json

url = "https://uat-connect.terrapay.com:21211/eig/gsma/transactions"

payload = json.dumps({
  "amount": "500",
  "currency": "INR",
  "type": "b2p",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId003",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {
    "subjectName": {
      "firstName": "Deepa",
      "lastName": "Jain",
      "fullName": "Deepa Jain"
    }
  },
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {}
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NZWQLJ42P1F",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```
```java
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"amount\": \"500\",\r\n    \"currency\": \"INR\",\r\n    \"type\": \"b2p\",\r\n    \"descriptionText\": \"Gift for my brother\",\r\n    \"requestDate\": \"2021-05-23 08:19:36\",\r\n    \"requestingOrganisationTransactionReference\": \"SrcTxnId003\",\r\n    \"debitParty\": [\r\n        {\r\n\t\t\"key\": \"msisdn\",\r\n\t\t\"value\": \"+4491509874561\"\r\n\t} \r\n    ],\r\n    \"creditParty\": [\r\n        {\r\n\t\t\"key\": \"msisdn\",\r\n\t\t\"value\": \"+2349061114853\"\r\n\t\t}\r\n    ],\r\n    \"senderKyc\": {},\r\n    \"recipientKyc\": {\r\n        \"subjectName\": {\r\n            \"firstName\": \"Deepa\",\r\n            \"lastName\": \"Jain\",\r\n            \"fullName\": \"Deepa Jain\"\r\n        }\r\n    },\r\n    \"sendingAmount\": \"35500.00\",\r\n    \"payinCcyCode\": \"USD\",\r\n    \"paymentMode\": \"cash\",\r\n    \"authenticationPartnerCode\": \"4534\",\r\n    \"paymentOption\": \"Mobile Wallet\",\r\n    \"sendingPartnerCode\": \"343432223\",\r\n    \"receivingPartnerCode\": \"343432223\",\r\n    \"business\": {\r\n        \"senderKyc\": {\r\n            \"businessName\": \"sample business\",\r\n            \"businessAddress1\": \"alton's road\",\r\n            \"businessAddressCity\": \"Lyon\",\r\n            \"businessAddressCountryCode\": \"US\",\r\n            \"businessPrimaryContactCountryCode\": \"US\",\r\n            \"businessPrimaryContactNo\": \"3472034605\",\r\n            \"businessDescription\": \"Electronics\",\r\n            \"businessCountryCode\": \"US\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"23123456789\",\r\n            \"businessRegistrationIssueDate\": \"2001-09-26\",\r\n            \"businessIDValidThru\": \"2033-09-26\",\r\n            \"businessEmail\":\"test@testemail.com\"\r\n        },\r\n        \"recepientKyc\": {}\r\n    },\r\n    \"internationalTransferInformation\": {\r\n        \"quoteId\": \"QR037C1NZWQLJ42P1F\",\r\n        \"receivingCountry\": \"IN\",\r\n        \"remittancePurpose\": \"Business Travel\",\r\n        \"sourceOfFunds\": \"Business Income\",\r\n        \"relationshipSender\": \"Employer\"\r\n    }\r\n}");
Request request = new Request.Builder()
  .url("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();
```
```ruby
require "uri"
require "json"
require "net/http"

url = URI("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")

https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true

request = Net::HTTP::Post.new(url)
request["Content-Type"] = "application/json"
request.body = JSON.dump({
  "amount": "500",
  "currency": "INR",
  "type": "b2p",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId003",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {},
  "recipientKyc": {
    "subjectName": {
      "firstName": "Deepa",
      "lastName": "Jain",
      "fullName": "Deepa Jain"
    }
  },
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {
      "businessName": "sample business",
      "businessAddress1": "alton's road",
      "businessAddressCity": "Lyon",
      "businessAddressCountryCode": "US",
      "businessPrimaryContactCountryCode": "US",
      "businessPrimaryContactNo": "3472034605",
      "businessDescription": "Electronics",
      "businessCountryCode": "US",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "23123456789",
      "businessRegistrationIssueDate": "2001-09-26",
      "businessIDValidThru": "2033-09-26",
      "businessEmail": "test@testemail.com"
    },
    "recepientKyc": {}
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NZWQLJ42P1F",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})

response = https.request(request)
puts response.read_body

```

### URL
https://uat-connect.terrapay.com:21211/eig/gsma/transactions
### HTTP Request
`POST /eig/gsma/transactions HTTP/1.1 `

## P2B transaction to bank 
### P2B transaction to bank <a class="tryitbutton" href='https://developers.terrapay.com/try-it/p2b-transaction-bank' target="_blank">Try it </a>


> P2B transaction to bank


```shell
 curl --location --request POST 'https://uat-connect.terrapay.com:21211/eig/gsma/transactions'\
 --header 'X-USERNAME: terrapayuser'\
 --header 'X-PASSWORD:
 101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825'\
--header 'X-DATE: 2017-05-03 11:00:00'\
--header 'X-ORIGINCOUNTRY:FR'\
--header 'Content-Type: application/json'\
--data-raw
{
	"currency": "NGN",
	"type": "p2b",
	"requestDate": "2020-01-02 10:51:16",
	"amount": "35500.00",
	"descriptionText": "Gift for my brother",
	"requestingOrganisationTransactionReference": "123458w8378400387553",
	"sendingAmount": "35500.00",
	"payinCcyCode": "USD",
	"provider": "23401",
	"paymentMode": "cash",
	"authenticationPartnerCode": "4534",
	"paymentOption": "Mobile Wallet",
	"sendingPartnerCode": "343432223",
	"receivingPartnerCode": "343432223",
	"debitParty": [
	{
		"key": "msisdn",
		"value": "+4491509874561"
	} 
	],
		"creditParty": [
	{
		"key": "bankaccountno",
		"value": "1976010126"
	},
	{
		"key": "sortcode",
		"value": "CITINGLA"
	},
	{
		"key": "organisationid",
		"value": "Citi Bank"
	},
	{
		"key": "banksubcode",
		"value": "0001"
	},
	{
		"key": "bankBranchName",
		"value": "Citi Bank"
	},
	{
		"key": "accountName",
		"value": "Rajesh"
	},
	{
		"key": "accountIBAN",
		"value": "GB29NWBK60161331926819"
	},
	{
		"key": "accountAdditionalNo1",
		"value": "2656915085434"
	}
	],
	"senderKyc": {
		"nationality": "US",
		"dateOfBirth": "1986-06-28",
		"gender": "M",
		"primaryContactCountryCode": "NG",
		"primaryContactNo": "2349061114853",
		"primaryContactNoType": "personal",
		"idDocument": [
			{
				"idType": "nationalidcard",
				"idNumber": "123456789",
				"issueDate": "2003-09-26",
				"expiryDate": "2033-09-26",
				"issuerCountry": "US"
			}
		],
		"postalAddress": {
			"addressLine1": "49",
			"addressLine2": "park street",
			"addressLine3": "walton's road",
			"city": "Lyon",
			"stateProvince": "Lyon",
			"postalCode": "123456",
			"country": "US"
		},
		"subjectName": {
			"title": "Mr.",
			"firstName": "Einstein",
			"middleName": "James",
			"lastName": "Bela",
			"fullName": "Einstien James Bela"
		}
	},
	"recipientKyc":{

	},
	"internationalTransferInformation":{
		"quoteId": "QT0FEO4TUIMN33Z6B",
		"receivingCountry": "NG",
		"remittancePurpose": "Business profits to Parents",
		"sourceOfFunds": "Savings",
		"relationshipSender": "Brother"
	},
	"business": {
		"senderKyc": {

		},
		"recepientKyc": {
			"businessName": "oyugi randy",
			"businessPINCode": "123456",
			"businessAddress1": "24",
			"businessAddress2": "walton's road",
			"businessAddressCity": "newyork",
			"businessAddressState": "NYC",
			"businessAddressCountryCode": "NG",
			"businessAddressZip": "123456",
			"businessPrimaryContactCountryCode": "NG",
			"businessPrimaryContactNo": "232323212",
			"businessPrimaryContactNoType": "Mobile",
			"businessDescription": "Electronics wholesale",
			"businessEmail": "vrs.electronics@gmail.com",
			"businessCountryCode": "NG",
			"businessRegistrationType": "p2b",
			"businessRegistrationNumber": "2312345678912",
			"businessRegistrationIssuedBy": "NYC_TRADE",
			"businessRegistrationIssuedAt": "NYC",
			"businessRegistrationIssueDate": "2002-09-26",
			"businessIDValidThru": "2036-09-26",
			"typeofbusiness": "Electronics",
			"businessPObox": "12345",
			"businessMobile": "343234433"
		}
	}
}

```

```javascript
var myHeaders = new Headers();
myHeaders.append("X-USERNAME", "terrapayuser");
myHeaders.append("X-PASSWORD", "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b");
myHeaders.append("X-DATE", "2018-04-04 09:27:16");
myHeaders.append("X-ORIGINCOUNTRY", "US");
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "amount": "500",
  "currency": "INR",
  "type": "p2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId005",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {
    "nationality": "AE",
    "dateOfBirth": "1967-05-28",
    "gender": "M",
    "idDocument": [
      {
        "idType": "VOTER_CARD",
        "idNumber": "13321115521",
        "issueDate": "1967-05-28",
        "expiryDate": "2067-05-28",
        "issuerCountry": "AE"
      }
    ],
    "postalAddress": {
      "addressLine1": "49 , park street",
      "addressLine2": "12",
      "addressLine3": "12",
      "city": "12",
      "stateProvince": "12",
      "postalCode": "50000",
      "country": "US"
    },
    "subjectName": {
      "firstName": "Test",
      "middleName": "",
      "lastName": "Sender2",
      "fullName": "Test Sender2"
    }
  },
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {},
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA6ZXBSQ88B",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://uat-connect.terrapay.com:21211/eig/gsma/transactions", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
```python
import requests
import json

url = "https://uat-connect.terrapay.com:21211/eig/gsma/transactions"

payload = json.dumps({
  "amount": "500",
  "currency": "INR",
  "type": "p2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId005",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {
    "nationality": "AE",
    "dateOfBirth": "1967-05-28",
    "gender": "M",
    "idDocument": [
      {
        "idType": "VOTER_CARD",
        "idNumber": "13321115521",
        "issueDate": "1967-05-28",
        "expiryDate": "2067-05-28",
        "issuerCountry": "AE"
      }
    ],
    "postalAddress": {
      "addressLine1": "49 , park street",
      "addressLine2": "12",
      "addressLine3": "12",
      "city": "12",
      "stateProvince": "12",
      "postalCode": "50000",
      "country": "US"
    },
    "subjectName": {
      "firstName": "Test",
      "middleName": "",
      "lastName": "Sender2",
      "fullName": "Test Sender2"
    }
  },
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {},
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA6ZXBSQ88B",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})
headers = {
  'X-USERNAME': 'terrapayuser',
  'X-PASSWORD': '101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b',
  'X-DATE': '2018-04-04 09:27:16',
  'X-ORIGINCOUNTRY': 'US',
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```
```java
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"amount\": \"500\",\r\n    \"currency\": \"INR\",\r\n    \"type\": \"p2b\",\r\n    \"descriptionText\": \"Gift for my brother\",\r\n    \"requestDate\": \"2021-05-23 08:19:36\",\r\n    \"requestingOrganisationTransactionReference\": \"SrcTxnId005\",\r\n    \"debitParty\": [\r\n        {\r\n            \"key\": \"msisdn\",\r\n            \"value\": \"+971810456234\"\r\n        }\r\n    ],\r\n    \"creditParty\": [\r\n        {\r\n            \"key\": \"bankaccountno\",\r\n            \"value\": \"50100002965304\"\r\n        },\r\n        {\r\n            \"key\": \"organisationid\",\r\n            \"value\": \"HDFC Bank\"\r\n        },\r\n        {\r\n            \"key\": \"sortcode\",\r\n            \"value\": \"HDFC0001626\"\r\n        }\r\n    ],\r\n    \"senderKyc\": {\r\n        \"nationality\": \"AE\",\r\n        \"dateOfBirth\": \"1967-05-28\",\r\n        \"gender\": \"M\",\r\n        \"idDocument\": [\r\n            {\r\n                \"idType\": \"VOTER_CARD\",\r\n                \"idNumber\": \"13321115521\",\r\n                \"issueDate\": \"1967-05-28\",\r\n                \"expiryDate\": \"2067-05-28\",\r\n                \"issuerCountry\": \"AE\"\r\n            }\r\n        ],\r\n        \"postalAddress\": {\r\n            \"addressLine1\": \"49 , park street\",\r\n            \"addressLine2\": \"12\",\r\n            \"addressLine3\": \"12\",\r\n            \"city\": \"12\",\r\n            \"stateProvince\": \"12\",\r\n            \"postalCode\": \"50000\",\r\n            \"country\": \"US\"\r\n        },\r\n        \"subjectName\": {\r\n            \"firstName\": \"Test\",\r\n            \"middleName\": \"\",\r\n            \"lastName\": \"Sender2\",\r\n            \"fullName\": \"Test Sender2\"\r\n        }\r\n    },\r\n    \"recipientKyc\": {},\r\n    \"sendingAmount\": \"35500.00\",\r\n    \"payinCcyCode\": \"USD\",\r\n    \"paymentMode\": \"cash\",\r\n    \"authenticationPartnerCode\": \"4534\",\r\n    \"paymentOption\": \"Mobile Wallet\",\r\n    \"sendingPartnerCode\": \"343432223\",\r\n    \"receivingPartnerCode\": \"343432223\",\r\n    \"business\": {\r\n        \"senderKyc\": {},\r\n        \"recepientKyc\": {\r\n            \"businessName\": \"Oyugi Randy Electric Sale Pvt. Ltd.\",\r\n            \"businessPINCode\": \"123456\",\r\n            \"businessAddress1\": \"24\",\r\n            \"businessAddress2\": \"walton's road\",\r\n            \"businessAddressCity\": \"newyork\",\r\n            \"businessAddressState\": \"NYC\",\r\n            \"businessAddressCountryCode\": \"NG\",\r\n            \"businessAddressZip\": \"123456\",\r\n            \"businessPrimaryContactCountryCode\": \"NG\",\r\n            \"businessPrimaryContactNo\": \"232323212\",\r\n            \"businessPrimaryContactNoType\": \"Mobile\",\r\n            \"businessDescription\": \"Electronics wholesale\",\r\n            \"businessEmail\": \"rs.electronics@gmail.com\",\r\n            \"businessCountryCode\": \"NG\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"2312345678912\",\r\n            \"businessRegistrationIssuedBy\": \"NYC_TRADE\",\r\n            \"businessRegistrationIssuedAt\": \"NYC\",\r\n            \"businessRegistrationIssueDate\": \"2002-08-26\",\r\n            \"businessIDValidThru\": \"2036-09-26\",\r\n            \"typeofbusiness\": \"Electronics\",\r\n            \"businessPObox\": \"12345\",\r\n            \"businessMobile\": \"343234433\"\r\n        }\r\n    },\r\n    \"internationalTransferInformation\": {\r\n        \"quoteId\": \"QR037C1NA6ZXBSQ88B\",\r\n        \"receivingCountry\": \"IN\",\r\n        \"remittancePurpose\": \"Business Travel\",\r\n        \"sourceOfFunds\": \"Business Income\",\r\n        \"relationshipSender\": \"Employer\"\r\n    }\r\n}");
Request request = new Request.Builder()
  .url("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")
  .method("POST", body)
  .addHeader("X-USERNAME", "terrapayuser")
  .addHeader("X-PASSWORD", "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b")
  .addHeader("X-DATE", "2018-04-04 09:27:16")
  .addHeader("X-ORIGINCOUNTRY", "US")
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();
```
```ruby
require "uri"
require "json"
require "net/http"

url = URI("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")

https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true

request = Net::HTTP::Post.new(url)
request["X-USERNAME"] = "terrapayuser"
request["X-PASSWORD"] = "101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b"
request["X-DATE"] = "2018-04-04 09:27:16"
request["X-ORIGINCOUNTRY"] = "US"
request["Content-Type"] = "application/json"
request.body = JSON.dump({
  "amount": "500",
  "currency": "INR",
  "type": "p2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId005",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+971810456234"
    }
  ],
  "creditParty": [
    {
      "key": "bankaccountno",
      "value": "50100002965304"
    },
    {
      "key": "organisationid",
      "value": "HDFC Bank"
    },
    {
      "key": "sortcode",
      "value": "HDFC0001626"
    }
  ],
  "senderKyc": {
    "nationality": "AE",
    "dateOfBirth": "1967-05-28",
    "gender": "M",
    "idDocument": [
      {
        "idType": "VOTER_CARD",
        "idNumber": "13321115521",
        "issueDate": "1967-05-28",
        "expiryDate": "2067-05-28",
        "issuerCountry": "AE"
      }
    ],
    "postalAddress": {
      "addressLine1": "49 , park street",
      "addressLine2": "12",
      "addressLine3": "12",
      "city": "12",
      "stateProvince": "12",
      "postalCode": "50000",
      "country": "US"
    },
    "subjectName": {
      "firstName": "Test",
      "middleName": "",
      "lastName": "Sender2",
      "fullName": "Test Sender2"
    }
  },
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {},
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA6ZXBSQ88B",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})

response = https.request(request)
puts response.read_body

```
### URL
https://uat-connect.terrapay.com:21211/eig/gsma/transactions
### HTTP Request
`POST /eig/gsma/transactions HTTP/1.1 `

## P2B transaction to mobile wallet
###  P2B transaction to mobile wallet <a class="tryitbutton" href='https://developers.terrapay.com/try-it/p2b-transaction-mobile' target="_blank">Try it </a>


> P2B transaction to mobile wallet 



```shell
curl --location --request POST 'https://uat-connect.terrapay.com:21211/eig/gsma/transactions'\
--header 'X-USERNAME: terrapayuser'\
--header 'X-PASSWORD: 101dfd2422f23f06120b77ab17d39229ff9bb40563eae042bc6cc6e8f9f1825b'\
--header 'X-DATE: 2019-08-25 12:00:00'\
--header 'X-ORIGINCOUNTRY:FR'\
--header 'Content-Type: application/json'\
--data--raw
{
	"currency": "NGN",
	"type": "p2b",
	"requestDate": "2020-01-02 10:51:16",
	"amount": "35500.00",
	"descriptionText": "Gift for my brother",
	"requestingOrganisationTransactionReference": "123458w8378400387553",
	"sendingAmount": "35500.00",
	"payinCcyCode": "USD",
	"provider": "23401",
	"paymentMode": "cash",
	"authenticationPartnerCode": "4534",
	"paymentOption": "Mobile Wallet",
	"sendingPartnerCode": "343432223",
	"receivingPartnerCode": "343432223",
	"debitParty": [
	{
		"key": "msisdn",
		"value": "+4491509874561"
	} 
	],
		"creditParty": [
	{
		"key": "msisdn",
		"value": "+2349061114853"
	}
	],
	"senderKyc": {
		"nationality": "US",
		"dateOfBirth": "1986-06-28",
		"gender": "M",
		"primaryContactCountryCode": "NG",
		"primaryContactNo": "2349061114853",
		"primaryContactNoType": "personal",
		"idDocument": [
			{
				"idType": "nationalidcard",
				"idNumber": "123456789",
				"issueDate": "2003-09-26",
				"expiryDate": "2033-09-26",
				"issuerCountry": "US"
			}
		],
		"postalAddress": {
			"addressLine1": "49",
			"addressLine2": "park street",
			"addressLine3": "walton's road",
			"city": "Lyon",
			"stateProvince": "Lyon",
			"postalCode": "123456",
			"country": "US"
		},
		"subjectName": {
			"title": "Mr.",
			"firstName": "Einstein",
			"middleName": "James",
			"lastName": "Bela",
			"fullName": "Einstien James Bela"
		}
	},
	"recipientKyc":{

	},
	"internationalTransferInformation":{
		"quoteId": "QT0FEO4TUIMN33Z6B",
		"receivingCountry": "NG",
		"remittancePurpose": "Business profits to Parents",
		"sourceOfFunds": "Savings",
		"relationshipSender": "Brother"
	},
	"business": {
		"senderKyc": {

		},
		"recepientKyc": {
			"businessName": "Kevin Hawkins",
			"businessPINCode": "123456",
			"businessAddress1": "24",
			"businessAddress2": "walton's road",
			"businessAddressCity": "newyork",
			"businessAddressState": "NYC",
			"businessAddressCountryCode": "NG",
			"businessAddressZip": "123456",
			"businessPrimaryContactCountryCode": "NG",
			"businessPrimaryContactNo": "232323212",
			"businessPrimaryContactNoType": "Mobile",
			"businessDescription": "Electronics wholesale",
			"businessEmail": "vrs.electronics@gmail.com",
			"businessCountryCode": "NG",
			"businessRegistrationType": "p2b",
			"businessRegistrationNumber": "2312345678912",
			"businessRegistrationIssuedBy": "NYC_TRADE",
			"businessRegistrationIssuedAt": "NYC",
			"businessRegistrationIssueDate": "2002-09-26",
			"businessIDValidThru": "2036-09-26",
			"typeofbusiness": "Electronics",
			"businessPObox": "12345",
			"businessMobile": "343234433"
		}
	}
}

```
```javascript
var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "amount": "500",
  "currency": "INR",
  "type": "p2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId005",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {
    "nationality": "AE",
    "dateOfBirth": "1967-05-28",
    "gender": "M",
    "idDocument": [
      {
        "idType": "VOTER_CARD",
        "idNumber": "13321115521",
        "issueDate": "1967-05-28",
        "expiryDate": "2067-05-28",
        "issuerCountry": "AE"
      }
    ],
    "postalAddress": {
      "addressLine1": "49 , park street",
      "addressLine2": "12",
      "addressLine3": "12",
      "city": "12",
      "stateProvince": "12",
      "postalCode": "50000",
      "country": "US"
    },
    "subjectName": {
      "firstName": "Test",
      "middleName": "",
      "lastName": "Sender2",
      "fullName": "Test Sender2"
    }
  },
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {},
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA6ZXBSQ88B",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://uat-connect.terrapay.com:21211/eig/gsma/transactions", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```
```python
import requests
import json

url = "https://uat-connect.terrapay.com:21211/eig/gsma/transactions"

payload = json.dumps({
  "amount": "500",
  "currency": "INR",
  "type": "p2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId005",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {
    "nationality": "AE",
    "dateOfBirth": "1967-05-28",
    "gender": "M",
    "idDocument": [
      {
        "idType": "VOTER_CARD",
        "idNumber": "13321115521",
        "issueDate": "1967-05-28",
        "expiryDate": "2067-05-28",
        "issuerCountry": "AE"
      }
    ],
    "postalAddress": {
      "addressLine1": "49 , park street",
      "addressLine2": "12",
      "addressLine3": "12",
      "city": "12",
      "stateProvince": "12",
      "postalCode": "50000",
      "country": "US"
    },
    "subjectName": {
      "firstName": "Test",
      "middleName": "",
      "lastName": "Sender2",
      "fullName": "Test Sender2"
    }
  },
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {},
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA6ZXBSQ88B",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data=payload)

print(response.text)

```
```java
OkHttpClient client = new OkHttpClient().newBuilder()
  .build();
MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\r\n    \"amount\": \"500\",\r\n    \"currency\": \"INR\",\r\n    \"type\": \"p2b\",\r\n    \"descriptionText\": \"Gift for my brother\",\r\n    \"requestDate\": \"2021-05-23 08:19:36\",\r\n    \"requestingOrganisationTransactionReference\": \"SrcTxnId005\",\r\n    \"debitParty\": [\r\n       {\r\n\t\t\"key\": \"msisdn\",\r\n\t\t\"value\": \"+4491509874561\"\r\n\t} \r\n    ],\r\n    \"creditParty\": [\r\n        {\r\n\t\t\"key\": \"msisdn\",\r\n\t\t\"value\": \"+2349061114853\"\r\n\t}\r\n        \r\n    ],\r\n    \"senderKyc\": {\r\n        \"nationality\": \"AE\",\r\n        \"dateOfBirth\": \"1967-05-28\",\r\n        \"gender\": \"M\",\r\n        \"idDocument\": [\r\n            {\r\n                \"idType\": \"VOTER_CARD\",\r\n                \"idNumber\": \"13321115521\",\r\n                \"issueDate\": \"1967-05-28\",\r\n                \"expiryDate\": \"2067-05-28\",\r\n                \"issuerCountry\": \"AE\"\r\n            }\r\n        ],\r\n        \"postalAddress\": {\r\n            \"addressLine1\": \"49 , park street\",\r\n            \"addressLine2\": \"12\",\r\n            \"addressLine3\": \"12\",\r\n            \"city\": \"12\",\r\n            \"stateProvince\": \"12\",\r\n            \"postalCode\": \"50000\",\r\n            \"country\": \"US\"\r\n        },\r\n        \"subjectName\": {\r\n            \"firstName\": \"Test\",\r\n            \"middleName\": \"\",\r\n            \"lastName\": \"Sender2\",\r\n            \"fullName\": \"Test Sender2\"\r\n        }\r\n    },\r\n    \"recipientKyc\": {},\r\n    \"sendingAmount\": \"35500.00\",\r\n    \"payinCcyCode\": \"USD\",\r\n    \"paymentMode\": \"cash\",\r\n    \"authenticationPartnerCode\": \"4534\",\r\n    \"paymentOption\": \"Mobile Wallet\",\r\n    \"sendingPartnerCode\": \"343432223\",\r\n    \"receivingPartnerCode\": \"343432223\",\r\n    \"business\": {\r\n        \"senderKyc\": {},\r\n        \"recepientKyc\": {\r\n            \"businessName\": \"Oyugi Randy Electric Sale Pvt. Ltd.\",\r\n            \"businessPINCode\": \"123456\",\r\n            \"businessAddress1\": \"24\",\r\n            \"businessAddress2\": \"walton's road\",\r\n            \"businessAddressCity\": \"newyork\",\r\n            \"businessAddressState\": \"NYC\",\r\n            \"businessAddressCountryCode\": \"NG\",\r\n            \"businessAddressZip\": \"123456\",\r\n            \"businessPrimaryContactCountryCode\": \"NG\",\r\n            \"businessPrimaryContactNo\": \"232323212\",\r\n            \"businessPrimaryContactNoType\": \"Mobile\",\r\n            \"businessDescription\": \"Electronics wholesale\",\r\n            \"businessEmail\": \"rs.electronics@gmail.com\",\r\n            \"businessCountryCode\": \"NG\",\r\n            \"businessRegistrationType\": \"Private Limited Company\",\r\n            \"businessRegistrationNumber\": \"2312345678912\",\r\n            \"businessRegistrationIssuedBy\": \"NYC_TRADE\",\r\n            \"businessRegistrationIssuedAt\": \"NYC\",\r\n            \"businessRegistrationIssueDate\": \"2002-08-26\",\r\n            \"businessIDValidThru\": \"2036-09-26\",\r\n            \"typeofbusiness\": \"Electronics\",\r\n            \"businessPObox\": \"12345\",\r\n            \"businessMobile\": \"343234433\"\r\n        }\r\n    },\r\n    \"internationalTransferInformation\": {\r\n        \"quoteId\": \"QR037C1NA6ZXBSQ88B\",\r\n        \"receivingCountry\": \"IN\",\r\n        \"remittancePurpose\": \"Business Travel\",\r\n        \"sourceOfFunds\": \"Business Income\",\r\n        \"relationshipSender\": \"Employer\"\r\n    }\r\n}");
Request request = new Request.Builder()
  .url("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")
  .method("POST", body)
  .addHeader("Content-Type", "application/json")
  .build();
Response response = client.newCall(request).execute();
```
```ruby
require "uri"
require "json"
require "net/http"

url = URI("https://uat-connect.terrapay.com:21211/eig/gsma/transactions")

https = Net::HTTP.new(url.host, url.port)
https.use_ssl = true

request = Net::HTTP::Post.new(url)
request["Content-Type"] = "application/json"
request.body = JSON.dump({
  "amount": "500",
  "currency": "INR",
  "type": "p2b",
  "descriptionText": "Gift for my brother",
  "requestDate": "2021-05-23 08:19:36",
  "requestingOrganisationTransactionReference": "SrcTxnId005",
  "debitParty": [
    {
      "key": "msisdn",
      "value": "+4491509874561"
    }
  ],
  "creditParty": [
    {
      "key": "msisdn",
      "value": "+2349061114853"
    }
  ],
  "senderKyc": {
    "nationality": "AE",
    "dateOfBirth": "1967-05-28",
    "gender": "M",
    "idDocument": [
      {
        "idType": "VOTER_CARD",
        "idNumber": "13321115521",
        "issueDate": "1967-05-28",
        "expiryDate": "2067-05-28",
        "issuerCountry": "AE"
      }
    ],
    "postalAddress": {
      "addressLine1": "49 , park street",
      "addressLine2": "12",
      "addressLine3": "12",
      "city": "12",
      "stateProvince": "12",
      "postalCode": "50000",
      "country": "US"
    },
    "subjectName": {
      "firstName": "Test",
      "middleName": "",
      "lastName": "Sender2",
      "fullName": "Test Sender2"
    }
  },
  "recipientKyc": {},
  "sendingAmount": "35500.00",
  "payinCcyCode": "USD",
  "paymentMode": "cash",
  "authenticationPartnerCode": "4534",
  "paymentOption": "Mobile Wallet",
  "sendingPartnerCode": "343432223",
  "receivingPartnerCode": "343432223",
  "business": {
    "senderKyc": {},
    "recepientKyc": {
      "businessName": "Oyugi Randy Electric Sale Pvt. Ltd.",
      "businessPINCode": "123456",
      "businessAddress1": "24",
      "businessAddress2": "walton's road",
      "businessAddressCity": "newyork",
      "businessAddressState": "NYC",
      "businessAddressCountryCode": "NG",
      "businessAddressZip": "123456",
      "businessPrimaryContactCountryCode": "NG",
      "businessPrimaryContactNo": "232323212",
      "businessPrimaryContactNoType": "Mobile",
      "businessDescription": "Electronics wholesale",
      "businessEmail": "rs.electronics@gmail.com",
      "businessCountryCode": "NG",
      "businessRegistrationType": "Private Limited Company",
      "businessRegistrationNumber": "2312345678912",
      "businessRegistrationIssuedBy": "NYC_TRADE",
      "businessRegistrationIssuedAt": "NYC",
      "businessRegistrationIssueDate": "2002-08-26",
      "businessIDValidThru": "2036-09-26",
      "typeofbusiness": "Electronics",
      "businessPObox": "12345",
      "businessMobile": "343234433"
    }
  },
  "internationalTransferInformation": {
    "quoteId": "QR037C1NA6ZXBSQ88B",
    "receivingCountry": "IN",
    "remittancePurpose": "Business Travel",
    "sourceOfFunds": "Business Income",
    "relationshipSender": "Employer"
  }
})

response = https.request(request)
puts response.read_body

```
### URL
https://uat-connect.terrapay.com:21211/eig/gsma/transactions
### HTTP Request
`POST /eig/gsma/transactions HTTP/1.1 `

## Business transaction request parameter list
### Business transaction request parameter list
Parameter name|	Description|Data Type|Requirement|Field Length
-------|----|-----|----|----
requestDate|The creation date and time of the transaction as supplied by the sending partner in YYYY-MM-DD HH:mm:ss format|String|Mandatory|19
amount|Destination amount payable to the beneficiary with precision of 2 decimal places.|String|Mandatory|10,2
currency|Destination amount currency in ISO 4217 format. Eg. NGN|String|Mandatory|3
type|The harmonized Transaction Type. Fixed value - b2b, b2p, p2b|String|Mandatory|3
descriptionText|Free format text description of the transaction provided by the client. This can be provided as a message for the receiver on the account statement.|String|Optional|	0-20
requestingOrganisationTransactionReference|Unique Transaction reference generated by the sending partner.|String|Mandatory|4-50
provider|Provider value should be same as sent in the validation request. If a different value is sent then the transaction will be rejected.|Numeric|Conditional|5-12
sendingAmount|Payin Amount with precision of 2 decimal places|String|Mandatory|10,2
payingCcyCode|Payin Currency in ISO 4217 format. Eg. USD|String|Mandatory|3
paymentMode|Type of Payment i.e. Cash, Card, Bank account or Others|String|Mandatory|0-20
authenticationPartnerCode|Multi factor authentication partner code. Unique code with a combination of 4 letters of the Company's first name, Country Code, City Code|	String|Optional|4-20
paymentOption|Mobile Wallet/Account Credit|String|Mandatory|4-100
sendingPartnerCode|Unique send partner code. Unique code with a combination of 4 letters of the Company's first name, Country Code, City Code|String|Optional|4-20
receivingPartnerCode|	Unique Receive Partner Code|String|Optional|4-20


### **debitParty:**

Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
key|msisdn|String|Mandatory|6
value|	Sender Mobile Number with country code. Eg. +91xxxxxxxxxx|String|Mandatory|10-18

### **creditParty:**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
Key|msisdn|String|Mandatory|6
Value|Beneficiary wallet Number with country code. Eg.+91xxxxxxxxxx.|String|Optional - For Bank Accounts Mandatory - For Mobile Wallet|5-50
Key|beneficiarySmsNotify|String|Optional|20
Value|Status Update through SMS notification. Values are true or false. true indicates notification required. Notification will be sent for b2b and p2b transactions on BusinessMsisdn number (part of business receipient kyc)|String | Optional|4-5
Key|bankaccountno|String|	Conditional|13
Value|Beneficiary bank account or IBAN number as applicable and required in the destination country for receiving funds. Eg. 2365417895 or AT483200000012345864. This key/value pair is optional if the transfer is to a mobile wallet.|String|Mandatory - For bank accounts Optional - For mobile wallets|5-50
Key|accounttype|String|Optional|11
Value|Type of the bank account. Supported account types:</br>Checking</br>Savings</br>The default account type for p2p transactions is Savings.|String||0-20
Key|sortcode|String|Conditional|8
Value|Bank Code as required in the destination Country. It is the IFSC code for India and Swift BIC for all other countries. The requirement of this code is destination country specific.|String|Mandatory - For bank accounts Optional - For mobile wallets|4-25
Key|organisationid|String|Conditional|14
Value|Full name of the beneficiary bank|String|Mandatory - For bank accounts Optional - For mobile wallets|4-60
Key|banksubcode|String|	Conditional|11
Value|This is a code that indicates the branch code or routing code or routing number of the specific bank branch to which the transaction is to be sent.<aside class="success"><strong>NOTE:</strong>  Mandatory for bank transactions to Bangladesh, Brazil & Uruguay. Optional for other countries. If the transaction is to Bangladesh then partner can send rounting number in banksubcode instead of sending the provider code</aside>|String|Mandatory - For bank accounts Optional - For mobile wallets|1-10
Key|accountIBAN|String |Conditional|11
Value|Recieve Account IBAN Number for receiving funds. This should be the same as the value in bankaccountno.|String |	Mandatory - For bank accounts Optional - For mobile wallets|13
Key|accountAdditionalNo1|String|Optional|20
Value|If any additional accounts to be provided.|String|Optional|13
Key|accountAdditionalNo2|String |Optional |20
Value|If any additional accounts to be provided.|String|Optional|13



### **senderKyc:** Applicable for p2b type transactions

Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
nationality|Nationality of the customer in ISO Alpha-2 format. Eg. US|String|Mandatory|2
dateOfBirth|Sender's Date of Birth in YYYY-MM-DD format|String|Mandatory|10
gender|Sender???s Gender. Enumeration = (M)ale, (F)emale, (U)nspecified|String|Optional|1
primaryContactCountryCode|Primary Contact Country Code|String|Mandatory|2
primaryContactNo|Primary Contact Number|String|Mandatory|10-15
primaryContactNoType|Primary Contact Number type i.e. Personal/Office|String|Mandatory|4-50
### **senderKyc:idDocument**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
idType|Sender???s Id document type: For example nationalidcard, drivinglicense, passport, etc|String|Mandatory|1-20
idNumber|Sender???s Id document number|String|Mandatory|1-30
issueDate|Sender???s Id document issue date in YYYY-MM-DD format.|String|Optional|10
expiryDate|Sender???s Id document expiry date in YYYY-MM-DD format.|String|Mandatory|10
issuerCountry|Country where the identification type was issued in ISO Alpha-2 format.|String|Optional|2
### **senderKyc:postalAddress**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
addressLine1|First line of the address|String|Mandatory|4-20
addressLine2|Second line of the address|String|Optional|4-20
addressLine3|Third line of the address|String|Optional|	4-20
city|City/Town of sender's address|String|Mandatory|4-20
stateProvince|State of sender's address|String|Optional|4-20
postalCode|Postal Code of sender's address|String|Optional|	6-8
country|Country in ISO Alpha-2 format|String|Mandatory|2
### **senderKyc:subjectName**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
title|Title of the Sender|String|Optional|0-6
firstName|First name of the Sender|String|Mandatory|1-20
middleName|Middle name of the Sender|	String|Optional|0-50
lastName|Last name of the Sender|String|Mandatory|1-20
fullName|Full name of the Sender|String|Mandatory|1-50
### **recipientKyc:** Applicable for b2p type transactions
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
nationality|Nationality of the customer in ISO Alpha-2 format. Eg. US |String|Optional|2
dateOfBirth|Beneficiary???s Date of Birth in YYYY-MM-DD format|String|Optional|10
gender|Beneficiary's Gender. Enumeration = (M)ale, (F)emale, (U)nspecified|String|Optional|1


### **recipientKyc:subjectName**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
firstName|First name of the beneficiary|String|Mandatory|1-20
lastName|Last name of the beneficiary|String|Mandatory|1-20
fullName|Full name of the beneficiary|String|Mandatory|1-50
### **recipientKyc:idDocument**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
idType|Beneficiary???s Id document as required in the destination country. Please <a href="#country-specific-recipient-documents" class="toc-h1 toc-link" data-title="Country Specific Recipient Documents"><b><i>click here</i></b></a> for the list of required document in each country.|String|Conditional|1-20
idNumber|Beneficiary???s Id document number|String|Conditional|1-30
issueDate|Beneficiary???s Id document issue date in YYYY-MM-DD format.|String|Optional|10
expiryDate|Beneficiary???s Id document expiry date in YYYY-MM-DD format.|String|Conditional|10
issuerCountry|	Country where the identification type was issued in ISO Alpha-2 format.|String|Optional|2
### **internationalTransferInformation:**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
quoteId|The specific quoteId to be used for the transaction. This quoteId is generated when a quotation is created and it is returned on the quotation response|String|Mandatory|16-20
receivingCountry|Destination country where the payout is to be made. To be specified in ISO Alpha 2 format. Eg. NG|String|Mandatory|2
remittancePurpose|Reason for the transfer. Click here to find the accepted values.|String|Mandatory|4-30
sourceOfFunds|Source of funds.|String|Mandatory|4-17
relationshipSender|The relation between the sender and the beneficiary.|String|Optional|3-11
### **businesssenderKyc: Applicable for b2p and b2b business transaction**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
businessName|Company Name|String|Mandatory|4-180
businessPINCode|Company Pin Code|String|Optional|2-20
businessAddress1|Registered Address 1|String|Mandatory|4-20
businessAddress2|Registered Address 2|String|Optional|4-20
businessAddressCity|Registered City|String|Optional|4-20
businessAddressCountryCode|Registered Country Code in ISO Alpha 2 standard|String|Optional|2
businessAddressZip|Registered address Zip Code|String|Optional|4-20
businessPrimaryContactCountryCode|Company Primary Contact Country Code in ISO Alpha 2 standard|String|Mandatory|2
businessPrimaryContactNo|Company Primary Contact Number|String|Mandatory|10-15
businessDescription|Short description of the business|String|	Optional|0-100
businessEmail|Company email id|String|Mandatory|0-100
businessCountryCode|Company Country Code in ISO Alpha 2 standard|String|Mandatory|2
businessRegistrationType|Type of Registration|String|Mandatory|4-100
businessRegistrationIssuedBy|Company Incorporation Issued by|String|Optional|0-20
businessRegistrationIssuedAt|Company Incorporation Issued at|String|Optional|0-20
businessRegistrationNumber|Company Incorporation Number|String|Mandatory|4-20
businessRegistrationIssueDate|Company Incorporation Issued Date in YYYY-MM-DD format.|String|	Optional|10
businessIDValidThru|Company Incorporation Expiry Date in YYYY-MM-DD format.|String|Mandatory|10
### **businessrecipientKyc:Applicable for p2b and b2b business transactions**
Parameter name|	Description|Data Type|Requirement|Field Length
----|----|---|---|---
business Name|Company Name|String|Mandatory|4-180
businessPINCode|Company Pin Code|String|Optional|2-20
businessAddress1|Registered Address 1|String|Optional|4-20
businessAddress2|Registered Address 2|String|Optional|4-20
businessAddressCity|Registered City	|String	|Optional|4-20
businessAddressState|Registered State|	String|	Optional|4-20
businessAddressCountryCode|	Registered Country Code in ISO Alpha 2 standard|String|	Mandatory|2
businessAddressZip|	Registered address Zip Code|String|	Optional|4-20
businessPrimaryContactCountryCode|Company Primary contact country code in ISO Alpha 2 standard|	String|	Optional|2
businessPrimaryContactNo|Company Primary Contact Number|String|	Optional|10-15
businessPrimaryContactNoType|Company Primary Contact Number type i.e. Personal/Office|String|Optional|4-50
businessDescription|Short description of the business|String|	Optional|0-100
businessEmail|Company email id|	String|	Optional|0-100	
businessCountryCode|Company country code in ISO Alpha 2 standard|String|Optional|2
businessRegistrationType|Type of Registration|String|Optional|0-100
businessRegistrationNumber|	Company Incorporation Number|String|Optional|0-20	
businessRegistrationIssuedBy|Company Incorporation Issued by|String|Optional|0-20
businessRegistrationIssuedAt|Company Incorporation Issued at|String|Optional|0-20
businessRegistrationIssueDate|Company Incorporation Issued Date|String|	Optional|0-10	
businessIDValidThru|Company Incorporation Expiry Date|String|Optional	|0-10
typeofbusiness|	Type of Company	|String|Optional|0-20	
business PO box	|Company PO Box	|String|Optional|0-10



