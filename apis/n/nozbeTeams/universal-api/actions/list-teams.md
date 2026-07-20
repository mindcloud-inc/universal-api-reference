# Nozbe Teams: List Teams

Retrieves accessible teams from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-teams?${params}`, {
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
      "avatarUrl": "https://example.com",
      "color": "string",
      "id": "string",
      "isPersonal": true,
      "isSharedTeam": true,
      "limits": "string",
      "name": "Ava Chen",
      "sidebarPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `color` | string |  |
| `id` | string |  |
| `isPersonal` | boolean |  |
| `isSharedTeam` | boolean |  |
| `limits` | string |  |
| `name` | string |  |
| `sidebarPosition` | number |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `GET /teams` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

