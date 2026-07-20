# redirect.pizza: Get Team Details



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-team-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-team-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-team-details?${params}`, {
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
      "hits": {},
      "hostnames": {},
      "id": 1,
      "name": "Ava Chen",
      "users": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hits` | object |  |
| `hostnames` | object |  |
| `id` | number |  |
| `name` | string |  |
| `users` | object |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/team` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-details.md) for the provider-specific parameters and requirements.

