# RevenueCat: Get App Public API Keys

Retrieves app public API keys from RevenueCat.

```
GET https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app-public-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RevenueCat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app-public-api-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app-public-api-keys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "string",
      "cancelled_at": "string",
      "code": "string",
      "created_at": "string",
      "deleted_at": "string",
      "display_name": "Ava Chen",
      "expires_at": "string",
      "id": "string",
      "items": [
        {}
      ],
      "metrics": [
        {}
      ],
      "name": "Ava Chen",
      "next_page": "string",
      "object": "string",
      "refunded_at": "string",
      "status": "string",
      "store_identifier": "string",
      "success": true,
      "updated_at": "string",
      "url": "https://example.com",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string |  |
| `cancelled_at` | string |  |
| `code` | string |  |
| `created_at` | string |  |
| `deleted_at` | string |  |
| `display_name` | string |  |
| `expires_at` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `metrics` | array<object> |  |
| `name` | string |  |
| `next_page` | string |  |
| `object` | string |  |
| `refunded_at` | string |  |
| `status` | string |  |
| `store_identifier` | string |  |
| `success` | boolean |  |
| `updated_at` | string |  |
| `url` | string |  |
| `value` | number |  |

## Native endpoint

Through the native RevenueCat API, this operation is `GET projects/:projectId/apps/:appId/public_api_keys` (base URL `https://api.revenuecat.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-app-public-api-keys.md) for the provider-specific parameters and requirements.

