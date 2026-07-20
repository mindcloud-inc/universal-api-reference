# SignalWire: Get FreeSWITCH Connector

Retrieves a FreeSWITCH connector from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-freeswitch-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-freeswitch-connector?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-freeswitch-connector?${params}`, {
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
| `id` | string | yes | Unique ID of a FreeSWITCH Connector. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "freeswitch_connector": {
        "caller_id": "string",
        "id": "string",
        "name": "Ava Chen",
        "send_as": "string"
      },
      "id": "string",
      "project_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the FreeSWITCH Connector Fabric Resource |
| `freeswitch_connector.caller_id` | string | Caller ID for the connector |
| `freeswitch_connector.id` | string | Unique ID of a FreeSWITCH Connector. |
| `freeswitch_connector.name` | string | Name of the FreeSWITCH Connector |
| `freeswitch_connector.send_as` | string | Send as identifier |
| `id` | string | Unique ID of the FreeSWITCH Connector. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/freeswitch_connectors/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-freeswitch-connector.md) for the provider-specific parameters and requirements.

