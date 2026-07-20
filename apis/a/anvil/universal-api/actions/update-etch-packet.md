# Anvil: Update Etch Packet

Updates an existing Etch packet in Anvil.

```
PUT https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-etch-packet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-etch-packet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.eid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anvil/latest/actions/update-etch-packet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.eid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.eid` | string | yes | Provide EID for Update Etch Packet. |
| `variables.token` | string | no | Provide Token for Update Etch Packet. |
| `variables.isArchived` | boolean | no | Provide Is Archived for Update Etch Packet. |
| `variables.name` | string | no | Provide Name for Update Etch Packet. |
| `variables.webhookURL` | string | no | Provide Webhook URL for Update Etch Packet. |
| `variables.payload` | object | no | Provide Payload for Update Etch Packet. |
| `variables.mergePayloads` | boolean | no | Provide Merge Payloads for Update Etch Packet. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-etch-packet.md) for the provider-specific parameters and requirements.

