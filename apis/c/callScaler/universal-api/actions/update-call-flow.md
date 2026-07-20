# CallScaler: Update Call Flow

Updates a call flow in CallScaler.

```
PUT https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/update-call-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/update-call-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/update-call-flow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no |  |
| `settings` | object | no | Call-flow settings such as recording, whisper, and press1. |
| `steps[]` | array<object> | no | Call-flow step configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_numbers": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "settings": {
        "press1": true,
        "recording": true,
        "whisper": true
      },
      "steps": [
        {
          "message": "string",
          "number": "string",
          "type": "string"
        }
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_numbers` | number | Number of assigned tracking numbers. |
| `created_at` | date | Call flow creation timestamp. |
| `id` | string | Unique call flow ID. |
| `name` | string | Call flow name. |
| `settings.press1` | boolean | Whether press-1 screening is enabled. |
| `settings.recording` | boolean | Whether recording is enabled. |
| `settings.whisper` | boolean | Whether whisper is enabled. |
| `steps[].message` | string | Step greeting or message text. |
| `steps[].number` | string | Forwarding phone number for a step. |
| `steps[].type` | string | Call flow step type. |
| `version` | number | Call flow version number. |

## Native endpoint

Through the native CallScaler API, this operation is `PUT /call-flows/:id` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-call-flow.md) for the provider-specific parameters and requirements.

