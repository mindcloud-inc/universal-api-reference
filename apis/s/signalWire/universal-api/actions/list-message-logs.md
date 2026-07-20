# SignalWire: List Message Logs

Retrieves message logs from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-message-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-message-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-message-logs?${params}`, {
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
| `includeDeleted` | boolean | no | Include logs for deleted activity. |
| `createdBefore` | string | no | Return logs for activity prior to this date. |
| `createdOn` | string | no | Return logs for activity on this date. |
| `createdAfter` | string | no | Return logs for activity after this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge": 1,
      "charge_details": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "from": "string",
      "id": "string",
      "kind": "string",
      "number_of_segments": 1,
      "source": "string",
      "status": "string",
      "to": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge` | number | The charge in dollars. |
| `charge_details` | array<object> | Details on charges associated with this log. |
| `created_at` | date | Date and time when the message entry was created. |
| `direction` | string | The direction of the message. |
| `from` | string | The origin phone number. |
| `id` | string | A unique identifier for the log. |
| `kind` | string | The kind of message. |
| `number_of_segments` | number | The number of segments. |
| `source` | string | Source of this log entry. |
| `status` | string | The status of the message. |
| `to` | string | The destination phone number. |
| `type` | string | Type of this log entry. |
| `url` | string | URL for the resource associated with this log entry (if available). |

## Native endpoint

Through the native SignalWire API, this operation is `GET /messaging/logs` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-logs.md) for the provider-specific parameters and requirements.

