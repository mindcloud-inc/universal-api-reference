# Swarm: Find Warm Paths by Company Website

Finds warm paths in Swarm by company website.

```
GET https://connect.mindcloud.co/v1/universal/swarm/latest/actions/find-warm-paths-by-company-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swarm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/find-warm-paths-by-company-website?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swarm/latest/actions/find-warm-paths-by-company-website?${params}`, {
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
      "items": [
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
| `count` | number |  |
| `items` | array<object> |  |
| `total_count` | number |  |

## Native endpoint

Through the native Swarm API, this operation is `POST /v2/profiles/network-mapper` (base URL `https://bee.theswarm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-warm-paths-by-company-website.md) for the provider-specific parameters and requirements.

