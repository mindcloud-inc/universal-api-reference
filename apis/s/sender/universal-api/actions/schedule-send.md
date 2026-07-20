# Sender: Schedule Send



```
PUT https://connect.mindcloud.co/v1/universal/sender/latest/actions/schedule-send
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sender/latest/actions/schedule-send" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "cmp_123",
  "scheduleTime": "2026-03-20 14:30:00"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/schedule-send', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "cmp_123",
    "scheduleTime": "2026-03-20 14:30:00"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Campaign ID. Example: `cmp_123`. |
| `scheduleTime` | date | yes | Send date and time in Y-m-d H:i:s format. Example: `2026-03-20 14:30:00`. |

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
| `message` | string | Success message returned when a Sender campaign schedule is updated. |

## Native endpoint

Through the native Sender API, this operation is `POST /campaigns/:id/schedule` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-send.md) for the provider-specific parameters and requirements.

