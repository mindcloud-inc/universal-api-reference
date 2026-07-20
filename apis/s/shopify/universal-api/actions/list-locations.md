# Shopify: List Locations

Retrieves locations from Shopify.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-locations?${params}`, {
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
| `locationQuery` | string | no | Optional raw Shopify locations query string, such as `name:Online` or `id:>=69379358899`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `afterCursor` | string | no | Optional cursor from the previous page to fetch the next page of locations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "fulfillsOnlineOrders": true,
      "id": "string",
      "isActive": true,
      "legacyResourceId": "string",
      "name": "Ava Chen",
      "nextCursor": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | When the location was created in Shopify. |
| `fulfillsOnlineOrders` | boolean | Whether the location can fulfill online orders. |
| `id` | string | Shopify location GID. |
| `isActive` | boolean | Whether the location is active. |
| `legacyResourceId` | string | Numeric Shopify location ID for later search steps. |
| `name` | string | Shopify location name. |
| `nextCursor` | string | Cursor to pass into After Cursor for the next page. |
| `updatedAt` | string | When the location was last updated in Shopify. |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

