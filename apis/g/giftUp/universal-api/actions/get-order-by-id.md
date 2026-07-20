# Gift Up: Get Order by ID



```
GET https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-order-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-order-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-order-by-id?${params}`, {
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customFields": [
        "string"
      ],
      "discount": 1,
      "downloadLinks": {},
      "id": "string",
      "metadata": {},
      "notes": [
        "string"
      ],
      "orderNumber": "string",
      "payment": {},
      "promotions": [
        "string"
      ],
      "purchaserEmail": "ava@example.com",
      "purchaserName": "Ava Chen",
      "referrer": "string",
      "revenue": 1,
      "salesTaxes": [
        "string"
      ],
      "selectedRecipient": "string",
      "serviceFee": 1,
      "shippingFee": 1,
      "tip": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `currency` | string |  |
| `customFields` | array<string> |  |
| `discount` | number |  |
| `downloadLinks` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `notes` | array<string> |  |
| `orderNumber` | string |  |
| `payment` | object |  |
| `promotions` | array<string> |  |
| `purchaserEmail` | string |  |
| `purchaserName` | string |  |
| `referrer` | string |  |
| `revenue` | number |  |
| `salesTaxes` | array<string> |  |
| `selectedRecipient` | string |  |
| `serviceFee` | number |  |
| `shippingFee` | number |  |
| `tip` | number |  |

## Native endpoint

Through the native Gift Up API, this operation is `GET /orders/:id` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-by-id.md) for the provider-specific parameters and requirements.

