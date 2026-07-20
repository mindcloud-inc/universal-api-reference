# Shippify: Get Delivery Quotes

Retrieves delivery quotes from Shippify for up to 100 deliveries.

```
GET https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-delivery-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-delivery-quotes?connectionId=$CONNECTION_ID&deliveries%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deliveries[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-delivery-quotes?${params}`, {
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
| `companyId` | number | no | Optional Shippify company identifier where the deliveries would be created. |
| `type` | string | no | Optional Shippify delivery type such as slot, express, or flex. |
| `deliveries[]` | array<object> | yes | Required array of Shippify delivery payload objects using the documented pickup, dropoff, packages, referenceId, tags, extraData, and cod structure. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveries": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "quoteId": 1,
      "timeWindows": [
        [
          {}
        ]
      ],
      "totalPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveries[]` | array<object> | Per-delivery quote breakdown. |
| `name` | string | Quote name. |
| `quoteId` | number | Quote identifier returned by Shippify. |
| `timeWindows[]` | array<object> | Available time windows for the quoted delivery option. |
| `totalPrice` | number | Total quoted price. |

## Native endpoint

Through the native Shippify API, this operation is `POST /v2/pricing/quotes/available` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-quotes.md) for the provider-specific parameters and requirements.

