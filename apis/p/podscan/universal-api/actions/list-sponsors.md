# Podscan: List Sponsors

Retrieves sponsor records from your Podscan account.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-sponsors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-sponsors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-sponsors?${params}`, {
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
      "count": 1,
      "limit": 1,
      "sort": "string",
      "sponsors": [
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
| `count` | number |  |
| `limit` | number |  |
| `sort` | string |  |
| `sponsors` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /sponsors` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sponsors.md) for the provider-specific parameters and requirements.

