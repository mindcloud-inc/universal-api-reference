# Datelist: List Products

Retrieves available products from Datelist by name or calendar.

```
GET https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datelist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datelist/latest/actions/list-products?${params}`, {
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
| `name` | string | no | Only return products matching a specific name. |
| `calendarId` | number | no | Only return products for a specific calendar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "calendarId": 1,
      "createdAt": "string",
      "deletedAt": "string",
      "description": "string",
      "duration": 1,
      "id": 1,
      "name": "Ava Chen",
      "places": 1,
      "price": 1,
      "taxAmount": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the product is active. |
| `calendarId` | number | Calendar ID. |
| `createdAt` | string | Creation timestamp. |
| `deletedAt` | string | Deletion timestamp, when present. |
| `description` | string | Product description. |
| `duration` | number | Duration in minutes. |
| `id` | number | Product ID. |
| `name` | string | Product name. |
| `places` | number | Available places. |
| `price` | number | Product price. |
| `taxAmount` | number | Tax amount. |
| `updatedAt` | string | Update timestamp. |

## Native endpoint

Through the native Datelist API, this operation is `GET /products` (base URL `https://datelist.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

