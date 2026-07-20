# Shopify: List Deleted Product Events

Retrieves deleted product events from Shopify.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-deleted-product-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-deleted-product-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-deleted-product-events?${params}`, {
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
| `query` | string | no | Shopify event search query. Defaults to deleted product events only and can be narrowed with created_at filters. Default: `action:'destroy' AND subject_type:'PRODUCT'`. Example: `action:'destroy' AND subject_type:'PRODUCT' AND created_at:>='2026-04-01'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "arguments": [
        [
          {}
        ]
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasNextCursor": true,
      "id": "string",
      "message": "string",
      "nextCursor": "string",
      "subjectId": "string",
      "subjectType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Shopify event action. For deleted products this is destroy. |
| `arguments[]` | array<object> | Additional event arguments returned by Shopify when present. |
| `createdAt` | date | When Shopify recorded the product deletion event. |
| `hasNextCursor` | boolean | Whether another page of deleted product events is available. |
| `id` | string | Shopify event GID for the deleted product event. |
| `message` | string | Event message returned by Shopify. |
| `nextCursor` | string | Cursor to pass into After Cursor for the next page of deleted product events. |
| `subjectId` | string | Deleted product GraphQL product ID. |
| `subjectType` | string | Shopify subject type for the deleted resource. |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deleted-product-events.md) for the provider-specific parameters and requirements.

