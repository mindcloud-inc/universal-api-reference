# Intruder: Snooze Issue Occurrence



```
PUT https://connect.mindcloud.co/v1/universal/intruder/latest/actions/snooze-issue-occurrence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/snooze-issue-occurrence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "issueId": "string",
  "id": "string",
  "reason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/snooze-issue-occurrence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "issueId": "string",
    "id": "string",
    "reason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issueId` | string | yes | The Intruder issue identifier. |
| `id` | string | yes | The Intruder occurrence identifier. |
| `reason` | string | yes | Why the occurrence is being snoozed. |
| `details` | string | no | Optional extra context for the snooze. |
| `duration` | number | no | How long to snooze the occurrence. |
| `durationType` | string | no | The unit for the snooze duration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `POST /issues/:issueId/occurrences/:id/snooze/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/snooze-issue-occurrence.md) for the provider-specific parameters and requirements.

