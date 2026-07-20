# Fourthwall: Get Order By Friendly ID

Retrieves an order from Fourthwall by friendly ID.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-order-by-friendly-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-order-by-friendly-id?connectionId=$CONNECTION_ID&friendlyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "friendlyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-order-by-friendly-id?${params}`, {
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
| `friendlyId` | string | yes | The order friendly ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailMarketingOptIn": true,
      "friendlyId": "string",
      "id": "string",
      "message": "string",
      "promotionId": "string",
      "shopId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutId` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailMarketingOptIn` | boolean |  |
| `friendlyId` | string |  |
| `id` | string |  |
| `message` | string |  |
| `promotionId` | string |  |
| `shopId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `username` | string |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/order/by-friendly-id/:friendlyId` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-by-friendly-id.md) for the provider-specific parameters and requirements.

