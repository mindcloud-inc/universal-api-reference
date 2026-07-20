# Jitbit Helpdesk: List Time Spent Log



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-time-spent-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-time-spent-log?connectionId=$CONNECTION_ID&ticketId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ticketId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-time-spent-log?${params}`, {
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
| `ticketId` | number | yes | Jitbit ticket ID to inspect time spent log for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "statusId": 1,
      "timeSpentInSeconds": 1,
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string | Log entry timestamp. |
| `statusId` | number | Ticket status ID at the time of the log entry. |
| `timeSpentInSeconds` | number | Time logged in seconds. |
| `userId` | number | Technician user ID. |
| `userName` | string | Technician username. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /TimeSpentLog` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-spent-log.md) for the provider-specific parameters and requirements.

