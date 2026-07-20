# SignalWire: Create PubSub Token

Creates a new PubSub token in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-pubsub-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-pubsub-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ttl": 1,
  "channels": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-pubsub-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ttl": 1,
    "channels": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ttl` | number | yes | The maximum time, in minutes, for which the access token will be valid. Between 1 and 43,200 (30 days). |
| `channels` | object | yes | Each channel with `write` and `read` objects with boolean as values. Max of 500 channels inside main `channels`. Either `read`, `write`, or both are required inside each channel and default to false. Each channel name can be up to 250 characters. Must be valid JSON. |
| `memberId` | string | no | The unique identifier of the member. Up to 250 characters. If not specified, a random UUID will be generated. |
| `state` | object | no | An arbitrary JSON object available to store stateful application information in. Must be valid JSON and have a maximum size of 2,000 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | A PubSub Token to be used to authenticate clients to the PubSub Service. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /pubsub/tokens` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pubsub-token.md) for the provider-specific parameters and requirements.

