# Gift Up: Get Report Transaction



```
GET https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-report-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-report-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-report-transaction?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "eventOccuredAtLocationId": "string",
      "eventOccuredOn": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "giftCard": {},
      "giftUpFee": 1,
      "id": "string",
      "metadata": {},
      "orderDetails": {},
      "orderId": "string",
      "reason": "string",
      "referrer": "string",
      "whoEmail": "ava@example.com",
      "whoName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `eventOccuredAtLocationId` | string |  |
| `eventOccuredOn` | date |  |
| `eventType` | string |  |
| `giftCard` | object |  |
| `giftUpFee` | number |  |
| `id` | string |  |
| `metadata` | object |  |
| `orderDetails` | object |  |
| `orderId` | string |  |
| `reason` | string |  |
| `referrer` | string |  |
| `whoEmail` | string |  |
| `whoName` | string |  |

## Native endpoint

Through the native Gift Up API, this operation is `GET /reports/transactions/:id` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-transaction.md) for the provider-specific parameters and requirements.

