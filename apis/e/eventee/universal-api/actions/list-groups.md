# Eventee: List Groups

Retrieves groups from Eventee.

```
GET https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-groups?${params}`, {
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
      "agenda": true,
      "color": "string",
      "emoji": "string",
      "gamification": true,
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "networking": true,
      "newsfeed": true,
      "publicName": "Ava Chen",
      "sessionRatings": true,
      "socialWall": true,
      "ticketNames": [
        "Ava Chen"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | boolean | Whether agenda is enabled for the group. |
| `color` | string | Group color value. |
| `emoji` | string | Group emoji. |
| `gamification` | boolean | Whether gamification is enabled for the group. |
| `id` | number | Group ID. |
| `isDefault` | boolean | Whether the group is the default group. |
| `name` | string | Internal group name. |
| `networking` | boolean | Whether networking is enabled for the group. |
| `newsfeed` | boolean | Whether newsfeed is enabled for the group. |
| `publicName` | string | Public group name. |
| `sessionRatings` | boolean | Whether session ratings are enabled for the group. |
| `socialWall` | boolean | Whether the social wall is enabled for the group. |
| `ticketNames` | array<string> | Ticket name list. |

## Native endpoint

Through the native Eventee API, this operation is `GET /groups` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

