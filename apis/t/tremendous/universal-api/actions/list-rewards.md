# Tremendous: List Rewards

Retrieves rewards from Tremendous.

```
GET https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tremendous `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-rewards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-rewards?${params}`, {
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
      "rewards": [
        {}
      ],
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rewards` | array<object> |  |
| `total_count` | number |  |

## Native endpoint

Through the native Tremendous API, this operation is `GET /rewards` (base URL `https://testflight.tremendous.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rewards.md) for the provider-specific parameters and requirements.

