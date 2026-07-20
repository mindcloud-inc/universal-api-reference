# Nozbe Teams: List Reminders

Retrieves accessible reminders from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-reminders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-reminders?${params}`, {
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
| `taskId` | string | no | Return only reminders for this task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isAllDay": true,
      "isRelative": true,
      "remindAt": 1,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `isRelative` | boolean |  |
| `remindAt` | number |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `GET /reminders` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reminders.md) for the provider-specific parameters and requirements.

