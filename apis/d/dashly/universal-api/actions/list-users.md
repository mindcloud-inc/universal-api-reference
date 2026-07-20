# Dashly: List Users

Retrieves users from a Dashly app.

```
GET https://connect.mindcloud.co/v1/universal/dashly/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/list-users?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashly/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Dashly application ID. |
| `idAsString` | boolean | no | Return IDs as strings. Default: `true`. |
| `offset` | number | no | Pagination start offset. |
| `limit` | number | no | Maximum number of users to fetch. Default: `20`. |
| `sortProp` | string | no | User property to sort by. Default: `$last_seen`. |
| `sortOrder` | string | no | Sort direction. Default: `desc`. |
| `convertPropsTypes` | boolean | no | Convert returned property values to native types. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "presence": "string",
      "props": {
        "$conversationsChats": 1,
        "$emailStatus": "ava@example.com",
        "$event2202217042021451294Count": 1,
        "$event2202217042021451294First": "string",
        "$event2202217042021451294Last": "string",
        "$event2202217042021451299Count": 1,
        "$event2202217042021451299First": "string",
        "$event2202217042021451299Last": "string",
        "$event2202217042021451308Count": 1,
        "$event2202217042021451308First": "string",
        "$event2202217042021451308Last": "string",
        "$event2202281793661437322Count": 1,
        "$event2202281793661437322First": "string",
        "$event2202281793661437322Last": "string",
        "$lastContacted": "string",
        "$lastReply": "string",
        "$lastSeen": "string",
        "$name": "Ava Chen",
        "$namePlaceholder": "Ava Chen",
        "$score": 1,
        "$sessions": 1,
        "$userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `presence` | string |  |
| `props.$conversationsChats` | number |  |
| `props.$emailStatus` | string |  |
| `props.$event2202217042021451294Count` | number |  |
| `props.$event2202217042021451294First` | string |  |
| `props.$event2202217042021451294Last` | string |  |
| `props.$event2202217042021451299Count` | number |  |
| `props.$event2202217042021451299First` | string |  |
| `props.$event2202217042021451299Last` | string |  |
| `props.$event2202217042021451308Count` | number |  |
| `props.$event2202217042021451308First` | string |  |
| `props.$event2202217042021451308Last` | string |  |
| `props.$event2202281793661437322Count` | number |  |
| `props.$event2202281793661437322First` | string |  |
| `props.$event2202281793661437322Last` | string |  |
| `props.$lastContacted` | string |  |
| `props.$lastReply` | string |  |
| `props.$lastSeen` | string |  |
| `props.$name` | string |  |
| `props.$namePlaceholder` | string |  |
| `props.$score` | number |  |
| `props.$sessions` | number |  |
| `props.$userId` | string |  |

## Native endpoint

Through the native Dashly API, this operation is `GET apps/:id/users` (base URL `https://api.dashly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

