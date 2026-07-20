# ChargeBee: List Usages

Retrieves usages from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-usages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-usages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-usages?${params}`, {
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
      "created_at": 1,
      "id": "string",
      "item_price_id": "string",
      "object": "string",
      "quantity": 1,
      "resource_version": 1,
      "subscription_id": "string",
      "usage_date": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `id` | string |  |
| `item_price_id` | string |  |
| `object` | string |  |
| `quantity` | number |  |
| `resource_version` | number |  |
| `subscription_id` | string |  |
| `usage_date` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET usages` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-usages.md) for the provider-specific parameters and requirements.

