# Reward Sciences: List Reward Categories



```
GET https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/list-reward-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/list-reward-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/list-reward-categories?${params}`, {
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
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Reward category records. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native Reward Sciences API, this operation is `GET /reward_categories` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reward-categories.md) for the provider-specific parameters and requirements.

