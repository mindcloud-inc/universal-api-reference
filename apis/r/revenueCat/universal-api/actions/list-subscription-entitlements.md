# RevenueCat: List Subscription Entitlements

Retrieves entitlements for a subscription in RevenueCat.

```
GET https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/list-subscription-entitlements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RevenueCat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/list-subscription-entitlements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/list-subscription-entitlements?${params}`, {
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
      "deleted_at": "string",
      "id": "string",
      "items": [
        {}
      ],
      "object": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted_at` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `object` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native RevenueCat API, this operation is `GET projects/:projectId/subscriptions/:subscriptionId/entitlements` (base URL `https://api.revenuecat.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscription-entitlements.md) for the provider-specific parameters and requirements.

