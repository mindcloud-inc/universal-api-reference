# ERPLY Books: Get VAT Rates

Retrieves VAT rates from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-vat-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-vat-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-vat-rates?${params}`, {
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
          "active": "string",
          "added": "string",
          "code": "string",
          "gstExemptTaxRateID": 1,
          "id": "string",
          "isReverseVat": 1,
          "lastModified": "string",
          "name": "Ava Chen",
          "rate": "string",
          "reverseRate": 1
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
| `records[].active` | string |  |
| `records[].added` | string |  |
| `records[].code` | string |  |
| `records[].gstExemptTaxRateID` | number |  |
| `records[].id` | string |  |
| `records[].isReverseVat` | number |  |
| `records[].lastModified` | string |  |
| `records[].name` | string |  |
| `records[].rate` | string |  |
| `records[].reverseRate` | number |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vat-rates.md) for the provider-specific parameters and requirements.

