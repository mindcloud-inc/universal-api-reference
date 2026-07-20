# Control D: List Profiles

Retrieves profiles from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-profiles?${params}`, {
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
      "name": "Ava Chen",
      "PK": "string",
      "profile": {},
      "stats": 1,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `PK` | string |  |
| `profile` | object |  |
| `stats` | number |  |
| `updated` | number |  |

## Native endpoint

Through the native Control D API, this operation is `GET /profiles` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-profiles.md) for the provider-specific parameters and requirements.

