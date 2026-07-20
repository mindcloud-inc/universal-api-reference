# Streamtime: Get Quote



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-quote?connectionId=$CONNECTION_ID&quoteId=1433522" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "quoteId": "1433522"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-quote?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | number | yes | Quote ID. Example: `1433522`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvedBy": "string",
      "approvedDatetime": "2026-05-07T12:00:00.000Z",
      "createdUser": "string",
      "currencyCode": "string",
      "currencySymbol": "string",
      "discount": 1,
      "exchangeRate": 1,
      "id": 1,
      "jobId": 1,
      "quoteCurrencyTotalAmountExTax": 1,
      "quoteCurrencyTotalAmountIncTax": 1,
      "quoteCurrencyTotalAmountTax": 1,
      "quoteDate": "string",
      "quoteName": "Ava Chen",
      "quoteNumber": "string",
      "quoteStatus": {},
      "sentByUserId": 1,
      "sentDatetime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvedBy` | string | Approver |
| `approvedDatetime` | date | Approved timestamp |
| `createdUser` | string | Display name of the quote creator |
| `currencyCode` | string | Currency code |
| `currencySymbol` | string | Currency symbol |
| `discount` | number | Discount percentage |
| `exchangeRate` | number | Exchange rate |
| `id` | number | Quote ID |
| `jobId` | number | Job ID |
| `quoteCurrencyTotalAmountExTax` | number | Total amount excluding tax |
| `quoteCurrencyTotalAmountIncTax` | number | Total amount including tax |
| `quoteCurrencyTotalAmountTax` | number | Total tax amount |
| `quoteDate` | string | Quote date |
| `quoteName` | string | Quote name |
| `quoteNumber` | string | Quote number |
| `quoteStatus` | object | Quote status object |
| `sentByUserId` | number | Sender user ID |
| `sentDatetime` | date | Quote sent timestamp |

## Native endpoint

Through the native Streamtime API, this operation is `GET /quotes/:quote_id` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quote.md) for the provider-specific parameters and requirements.

