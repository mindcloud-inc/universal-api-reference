# TickTick: List User Projects

Retrieves the user's projects from TickTick.

```
GET https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/list-user-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/list-user-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/list-user-projects?${params}`, {
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
      "closed": true,
      "color": "string",
      "groupId": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "permission": "string",
      "sortOrder": 1,
      "viewMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `color` | string |  |
| `groupId` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `permission` | string |  |
| `sortOrder` | number |  |
| `viewMode` | string |  |

## Native endpoint

Through the native TickTick API, this operation is `GET /open/v1/project` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-projects.md) for the provider-specific parameters and requirements.

