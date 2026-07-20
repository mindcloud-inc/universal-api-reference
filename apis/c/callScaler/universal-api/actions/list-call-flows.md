# CallScaler: List Call Flows

Retrieves call flows from CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-call-flows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-call-flows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-call-flows?${params}`, {
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

Through the native CallScaler API, this operation is `GET /call-flows` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-call-flows.md) for the provider-specific parameters and requirements.

