# SignalWire: Get Call Flow

Retrieves a call flow from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-call-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-call-flow?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-call-flow?${params}`, {
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
| `id` | string | yes | Unique ID of a Call Flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_flow": {
        "document_version": 1,
        "flow_data": "string",
        "id": "string",
        "relayml": "string",
        "title": "string"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
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
| `call_flow.document_version` | number | The current revision of the call flow. Every update must increase this number. |
| `call_flow.flow_data` | string | Call flow data as JSON string |
| `call_flow.id` | string | Unique ID of a Call Flow. |
| `call_flow.relayml` | string | A SWML document. For more information on SWML, please go to the [SWML docs](/swml) |
| `call_flow.title` | string | The name of the Call Flow |
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the Call Flow Fabric Resource |
| `id` | string | Unique ID of the Call Flow. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/call_flows/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-flow.md) for the provider-specific parameters and requirements.

