# Fourthwall: List Orders

Retrieves a paginated list of orders from Fourthwall.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-orders?${params}`, {
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
| `email` | string | no | Filter orders by customer email. |
| `createdAt[gt]` | date | no | Filter orders created after this timestamp. |
| `createdAt[lt]` | date | no | Filter orders created before this timestamp. |
| `updatedAt[gt]` | date | no | Filter orders updated after this timestamp. |
| `updatedAt[lt]` | date | no | Filter orders updated before this timestamp. |
| `status` | list | no | Filter orders by status. One of: `CANCELLED`, `COMPLETED`, `CONFIRMED`, `DELIVERED`, `IN_PRODUCTION`, `PARTIALLY_DELIVERED`, `PARTIALLY_IN_PRODUCTION`, `PARTIALLY_SHIPPED`, `SHIPPED`. Accepts multiple values as an array. |

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

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/order` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

