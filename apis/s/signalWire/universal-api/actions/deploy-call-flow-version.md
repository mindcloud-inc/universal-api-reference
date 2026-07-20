# SignalWire: Deploy Call Flow Version

Deploys a call flow version in SignalWire.

```
PUT https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/deploy-call-flow-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/deploy-call-flow-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "documentVersion": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/deploy-call-flow-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "documentVersion": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique identifier of the Call Flow. |
| `documentVersion` | number | yes | The current revision of the call flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "document_version": 1,
      "flow_data": "string",
      "id": "string",
      "relayml": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | The creation timestamp. |
| `document_version` | number | The document version. |
| `flow_data` | string | Call Flow data structure |
| `id` | string | The unique identifier of the deployed Call Flow Version. |
| `relayml` | string | SWML document for this version |
| `updated_at` | string | The last update timestamp. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/call_flow/{id}/versions` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deploy-call-flow-version.md) for the provider-specific parameters and requirements.

