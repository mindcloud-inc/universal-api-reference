# Novacal: List Teams

Retrieves teams from Novacal.

```
GET https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/list-teams?${params}`, {
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
      "about": "string",
      "id": 1,
      "logo": "string",
      "name": "Ava Chen",
      "username": "Ava Chen",
      "users": [
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
| `about` | string | Team description. |
| `id` | number | Team ID. |
| `logo` | string | Team logo URL. |
| `name` | string | Team name. |
| `username` | string | Team username. |
| `users` | array<object> | Team members. |

## Native endpoint

Through the native Novacal API, this operation is `GET /v1/teams` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

