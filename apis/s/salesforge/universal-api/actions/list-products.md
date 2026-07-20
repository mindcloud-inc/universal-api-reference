# Salesforge: List Products

Retrieves products from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=wks_lxxtq91neaixc8yaiqp7w" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-products?${params}`, {
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
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "internalName": "Ava Chen",
      "translations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `internalName` | string |  |
| `translations` | array<object> |  |

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/products` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

