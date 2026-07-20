# SignalWire: Send Call Commands

Sends call commands to SignalWire calls.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/send-call-commands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/send-call-commands" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "command": "string",
  "params.from": "string",
  "params.to": "string",
  "params.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/send-call-commands', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "command": "string",
    "params.from": "string",
    "params.to": "string",
    "params.url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `command` | string | yes | The `dial` command is used to create a new call. |
| `params.from` | string | yes | The address that initiated the call. Can be either a E.164 formatted number (`+xxxxxxxxxxx`), or a SIP endpoint (`sip:xxx@yyy.zzz`). |
| `params.to` | string | yes | The address that received the call. Can be either a E.164 formatted number (`+xxxxxxxxxxx`), or a SIP endpoint (`sip:xxx@yyy.zzz`). |
| `params.callerId` | string | no | The number, in E.164 format, or identifier of the caller. |
| `params.fallbackUrl` | string | no | The Fallback URL to handle the call. This parameter allows you to specify a backup webhook or different route in your code containing SWML instructions for handling the call. |
| `params.statusUrl` | string | no | A URL that will recieve status updates of the current call. Any call events defined in `status_events` will be delivered to the defined URL. |
| `params.statusEvents[]` | array<string> | no | The call events that will be monitored and sent to the `status_url` when active. |
| `params.url` | string | yes | The URL to handle the call. This parameter allows you to specify a webhook or different route in your code containing SWML instructions for handling the call. Either `url` or `swml` must be included for a new call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_ms": 1,
      "charge": 1,
      "charge_details": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "duration": 1,
      "duration_ms": 1,
      "from": "string",
      "id": "string",
      "parent_id": "string",
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
| `billing_ms` | number | The billable duration of the call in milliseconds. |
| `charge` | number | Total charge for this call. |
| `charge_details` | array<object> | Details on charges associated with this call. |
| `created_at` | date | The date and time when the call was created. |
| `direction` | string | The direction of the call. |
| `duration` | number | The duration of the call in seconds. |
| `duration_ms` | number | The duration of the call in milliseconds. |
| `from` | string | The origin number or address. |
| `id` | string | The unique identifier of the call on SignalWire. This can be used to update the call programmatically. |
| `parent_id` | string | The parent call ID if this is a child call. |
| `source` | string | Source of this call. |
| `status` | string | The status of the call. |
| `to` | string | The destination number or address. |
| `type` | string | Type of this call. |
| `url` | string | The URL associated with this call. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /calling/calls` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-call-commands.md) for the provider-specific parameters and requirements.

