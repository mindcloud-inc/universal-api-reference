# ERPLY Books: Get Company Info

Retrieves company information from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-company-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-company-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-company-info?${params}`, {
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
          "bankAccountNumber": "string",
          "bankAccountNumber2": "string",
          "bankIBAN": "string",
          "bankIBAN2": "string",
          "bankName": "Ava Chen",
          "bankName2": "Ava Chen",
          "bankSWIFT": "string",
          "bankSWIFT2": "string",
          "city": "string",
          "code": "string",
          "companyName": "Ava Chen",
          "companyTypeID": 1,
          "country": "string",
          "defaultClientID": 1,
          "defaultCurrency": "string",
          "eInvoiceAddress": "string",
          "email": "ava@example.com",
          "fax": "string",
          "id": "string",
          "intermediatorCode": "string",
          "invoiceRounding": 1,
          "mobile": "string",
          "name": "Ava Chen",
          "phone": "string",
          "state": "string",
          "street": "string",
          "VAT": "string",
          "web": "string",
          "ZIPcode": "string"
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
| `records[].bankAccountNumber` | string |  |
| `records[].bankAccountNumber2` | string |  |
| `records[].bankIBAN` | string |  |
| `records[].bankIBAN2` | string |  |
| `records[].bankName` | string |  |
| `records[].bankName2` | string |  |
| `records[].bankSWIFT` | string |  |
| `records[].bankSWIFT2` | string |  |
| `records[].city` | string |  |
| `records[].code` | string |  |
| `records[].companyName` | string |  |
| `records[].companyTypeID` | number |  |
| `records[].country` | string |  |
| `records[].defaultClientID` | number |  |
| `records[].defaultCurrency` | string |  |
| `records[].eInvoiceAddress` | string |  |
| `records[].email` | string |  |
| `records[].fax` | string |  |
| `records[].id` | string |  |
| `records[].intermediatorCode` | string |  |
| `records[].invoiceRounding` | number |  |
| `records[].mobile` | string |  |
| `records[].name` | string |  |
| `records[].phone` | string |  |
| `records[].state` | string |  |
| `records[].street` | string |  |
| `records[].VAT` | string |  |
| `records[].web` | string |  |
| `records[].ZIPcode` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-info.md) for the provider-specific parameters and requirements.

