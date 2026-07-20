# ERPLY Books: Get Customers

Retrieves customer records from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "address": "string",
          "address2": "string",
          "addressTypeID": 1,
          "addressTypeName": "Ava Chen",
          "birthday": "string",
          "city": "string",
          "code": "string",
          "colorStatus": "string",
          "companyName": "Ava Chen",
          "companyTypeID": 1,
          "country": "string",
          "countryID": "string",
          "credit": 1,
          "creditCardLastNumbers": "string",
          "customerBalanceDisabled": 1,
          "customerCardNumber": "string",
          "customerID": 1,
          "customerType": "string",
          "deliveryTypeID": 1,
          "docuraEDIEnabled": 1,
          "doNotSell": 1,
          "EDI": "string",
          "ediType": "string",
          "eInvoiceEmail": "ava@example.com",
          "eInvoiceEnabled": 1,
          "eInvoiceReference": "string",
          "email": "ava@example.com",
          "emailEnabled": 1,
          "emailOptOut": 1,
          "euCustomerType": "string",
          "facebookName": "Ava Chen",
          "factoringContractNumber": "string",
          "fax": "string",
          "firstName": "Ava",
          "flagStatus": 1,
          "fullName": "Ava Chen",
          "gender": "string",
          "GLN": "string",
          "groupID": 1,
          "groupName": "Ava Chen",
          "homeStoreID": 1,
          "id": 1,
          "image": "string",
          "integrationCode": "string",
          "isPOSDefaultCustomer": 1,
          "lastModifierEmployeeID": 1,
          "lastModifierUsername": "Ava Chen",
          "lastName": "Chen",
          "mailEnabled": 1,
          "mobile": "string",
          "operatorIdentifier": "string",
          "partialTaxExemption": 1,
          "payerID": 1,
          "paysViaFactoring": 1,
          "PeppolID": "string",
          "personTitleID": 1,
          "phone": "string",
          "posCouponsDisabled": 1,
          "postalCode": "string",
          "primaryStoreID": {},
          "referenceNumber": "string",
          "rewardPoints": 1,
          "rewardPointsDisabled": 1,
          "salesBlocked": 1,
          "secondaryStoreID": {},
          "signUpStoreID": 1,
          "state": "string",
          "street": "string",
          "taxExempt": 1,
          "twitterID": "string"
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].address` | string |  |
| `records[].address2` | string |  |
| `records[].addressTypeID` | number |  |
| `records[].addressTypeName` | string |  |
| `records[].birthday` | string |  |
| `records[].city` | string |  |
| `records[].code` | string |  |
| `records[].colorStatus` | string |  |
| `records[].companyName` | string |  |
| `records[].companyTypeID` | number |  |
| `records[].country` | string |  |
| `records[].countryID` | string |  |
| `records[].credit` | number |  |
| `records[].creditCardLastNumbers` | string |  |
| `records[].customerBalanceDisabled` | number |  |
| `records[].customerCardNumber` | string |  |
| `records[].customerID` | number |  |
| `records[].customerType` | string |  |
| `records[].deliveryTypeID` | number |  |
| `records[].docuraEDIEnabled` | number |  |
| `records[].doNotSell` | number |  |
| `records[].EDI` | string |  |
| `records[].ediType` | string |  |
| `records[].eInvoiceEmail` | string |  |
| `records[].eInvoiceEnabled` | number |  |
| `records[].eInvoiceReference` | string |  |
| `records[].email` | string |  |
| `records[].emailEnabled` | number |  |
| `records[].emailOptOut` | number |  |
| `records[].euCustomerType` | string |  |
| `records[].facebookName` | string |  |
| `records[].factoringContractNumber` | string |  |
| `records[].fax` | string |  |
| `records[].firstName` | string |  |
| `records[].flagStatus` | number |  |
| `records[].fullName` | string |  |
| `records[].gender` | string |  |
| `records[].GLN` | string |  |
| `records[].groupID` | number |  |
| `records[].groupName` | string |  |
| `records[].homeStoreID` | number |  |
| `records[].id` | number |  |
| `records[].image` | string |  |
| `records[].integrationCode` | string |  |
| `records[].isPOSDefaultCustomer` | number |  |
| `records[].lastModifierEmployeeID` | number |  |
| `records[].lastModifierUsername` | string |  |
| `records[].lastName` | string |  |
| `records[].mailEnabled` | number |  |
| `records[].mobile` | string |  |
| `records[].operatorIdentifier` | string |  |
| `records[].partialTaxExemption` | number |  |
| `records[].payerID` | number |  |
| `records[].paysViaFactoring` | number |  |
| `records[].PeppolID` | string |  |
| `records[].personTitleID` | number |  |
| `records[].phone` | string |  |
| `records[].posCouponsDisabled` | number |  |
| `records[].postalCode` | string |  |
| `records[].primaryStoreID` | object |  |
| `records[].referenceNumber` | string |  |
| `records[].rewardPoints` | number |  |
| `records[].rewardPointsDisabled` | number |  |
| `records[].salesBlocked` | number |  |
| `records[].secondaryStoreID` | object |  |
| `records[].signUpStoreID` | number |  |
| `records[].state` | string |  |
| `records[].street` | string |  |
| `records[].taxExempt` | number |  |
| `records[].twitterID` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customers.md) for the provider-specific parameters and requirements.

