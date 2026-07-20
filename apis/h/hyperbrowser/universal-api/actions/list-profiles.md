# Hyperbrowser: List Profiles



```
GET https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/list-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperbrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/list-profiles?${params}`, {
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
      "page": 1,
      "perPage": 1,
      "profiles": [
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
| `page` | number |  |
| `perPage` | number |  |
| `profiles` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Hyperbrowser API, this operation is `GET /api/profiles` (base URL `https://api.hyperbrowser.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-profiles.md) for the provider-specific parameters and requirements.

