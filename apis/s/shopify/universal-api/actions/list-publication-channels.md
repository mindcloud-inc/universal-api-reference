# Shopify: List Publication Channels

Retrieves publication channels from Shopify.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-publication-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-publication-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-publication-channels?${params}`, {
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
| `variables` | object | no | Container for Shopify GraphQL variables used by this action. |
| `variables.catalogType` | string | no | Optional Shopify catalog type filter. One of: `0`, `1`, `2`. |
| `variables.first` | number | no | Max publication channels to return in a single call. Default: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.after` | string | no | Optional cursor for manually fetching the next page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoPublish": true,
      "hasNextCursor": true,
      "id": "string",
      "name": "Ava Chen",
      "nextCursor": "string",
      "supportsFuturePublishing": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoPublish` | boolean | Whether new products auto-publish to this publication. |
| `hasNextCursor` | boolean | Whether another page is available. |
| `id` | string | Shopify publication channel GID. |
| `name` | string | Publication channel name. |
| `nextCursor` | string | Cursor to pass into After Cursor for the next page. |
| `supportsFuturePublishing` | boolean | Whether this publication supports future publishing dates. |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-publication-channels.md) for the provider-specific parameters and requirements.

