# SignalWire: List Fax Logs

Retrieves fax logs from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-fax-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-fax-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-fax-logs?${params}`, {
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
      "error_code": "string",
      "error_message": "string",
      "from": "string",
      "id": "string",
      "number_of_pages": 1,
      "quality": "string",
      "remote_station": "string",
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
| `charge` | number | The amount charge for this fax request. |
| `charge_details` | array<object> | Details on charges associated with this log. |
| `created_at` | date | Date and time when the fax was created. |
| `direction` | string | The direction of this fax call. |
| `error_code` | string | Error code for this resource (if available). |
| `error_message` | string | The description of this error (if available). |
| `from` | string | The origin phone number in E.164 format. |
| `id` | string | A unique identifier for the log |
| `number_of_pages` | number | The number of pages the fax document contained. |
| `quality` | string | The quality that was set when the fax document was sent. |
| `remote_station` | string | Represents a customer hosted Fax server |
| `source` | string | Source of this log entry. |
| `status` | string | The status of this fax call. |
| `to` | string | The destination phone number in E.164 format. |
| `type` | string | Type of this log entry. |
| `url` | string | URL for the associated fax resource with this log entry (if available) |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fax/logs` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fax-logs.md) for the provider-specific parameters and requirements.

