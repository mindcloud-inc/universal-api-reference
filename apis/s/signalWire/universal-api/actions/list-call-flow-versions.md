# SignalWire: List Call Flow Versions

Retrieves call flow versions from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-call-flow-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-call-flow-versions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-call-flow-versions?${params}`, {
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
| `id` | string | yes | The unique identifier of the Call Flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "flow_data": "string",
      "id": "string",
      "relayml": "string",
      "updated_at": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | The creation timestamp. |
| `flow_data` | string | Call Flow data structure |
| `id` | string | The unique identifier of the version. |
| `relayml` | string | SWML document for this version |
| `updated_at` | string | The last update timestamp. |
| `version` | string | The version number. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/call_flow/{id}/versions` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-call-flow-versions.md) for the provider-specific parameters and requirements.

