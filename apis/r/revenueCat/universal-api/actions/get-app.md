# RevenueCat: Get App

Retrieves an app from RevenueCat.

```
GET https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RevenueCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app?${params}`, {
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

Through the native RevenueCat API, this operation is `GET projects/:projectId/apps/:appId` (base URL `https://api.revenuecat.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

