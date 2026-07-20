# Reamaze: List Satisfaction Ratings



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-satisfaction-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-satisfaction-ratings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-satisfaction-ratings?${params}`, {
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
      "pageCount": 1,
      "pageSize": 1,
      "satisfactionRatings": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `satisfactionRatings` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /satisfaction_ratings` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-satisfaction-ratings.md) for the provider-specific parameters and requirements.

