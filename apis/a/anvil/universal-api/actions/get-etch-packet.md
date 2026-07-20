# Anvil: Get Etch Packet

Retrieves an Etch packet from Anvil.

```
GET https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-etch-packet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anvil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-etch-packet?connectionId=$CONNECTION_ID&variables.eid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.eid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anvil/latest/actions/get-etch-packet?${params}`, {
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
| `variables.eid` | string | yes | Provide EID for Get Etch Packet. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anvil API returns.

## Native endpoint

Through the native Anvil API, this operation is `POST /` (base URL `https://graphql.useanvil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-etch-packet.md) for the provider-specific parameters and requirements.

