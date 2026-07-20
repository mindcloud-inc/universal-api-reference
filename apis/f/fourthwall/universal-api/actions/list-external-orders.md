# Fourthwall: List External Orders

Retrieves external orders from Fourthwall with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-external-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-external-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-external-orders?${params}`, {
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
| `externalSource` | string | no | Filter external orders by source. |
| `externalOrderId` | string | no | Filter external orders by external order ID. |
| `status` | string | no | Filter external orders by status. Accepts multiple values as an array. |
| `createdAfter` | date | no | Filter external orders created after this timestamp. |
| `createdBefore` | date | no | Filter external orders created before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalOrderId": "string",
      "externalSource": "string",
      "friendlyId": "string",
      "orderId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `externalOrderId` | string |  |
| `externalSource` | string |  |
| `friendlyId` | string |  |
| `orderId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/external-orders` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-external-orders.md) for the provider-specific parameters and requirements.

