# Woztell: Create Channel

Creates a channel in your Woztell workspace.

```
POST https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | yes | GraphQL variables object. Use {"input":{"name":"..."}} and optionally include description, tags, app, info, meta, or on from CreateChannelInput. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woztell API returns.

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

