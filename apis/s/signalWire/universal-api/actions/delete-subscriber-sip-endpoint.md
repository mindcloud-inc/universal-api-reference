# SignalWire: Delete Subscriber SIP Endpoint

Deletes an existing subscriber SIP endpoint from SignalWire.

```
DELETE https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/delete-subscriber-sip-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/delete-subscriber-sip-endpoint?connectionId=$CONNECTION_ID&id=string&fabricSubscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "fabricSubscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/delete-subscriber-sip-endpoint?${params}`, {
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
| `id` | string | yes | Unique ID of a Sip Endpoint. |
| `fabricSubscriberId` | string | yes | Unique ID of a Fabric Subscriber. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SignalWire API returns.

## Native endpoint

Through the native SignalWire API, this operation is `DELETE /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber-sip-endpoint.md) for the provider-specific parameters and requirements.

