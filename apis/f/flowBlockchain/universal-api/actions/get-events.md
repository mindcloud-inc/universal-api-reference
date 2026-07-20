# Flow Blockchain: Get Events

Retrieves events from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-events?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-events?${params}`, {
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
| `endHeight` | string | no | End block height for event search. |
| `startHeight` | string | no | Start block height for event search. |
| `type` | string | yes | Fully qualified Flow event type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_height": "string",
      "block_id": "string",
      "block_timestamp": "2026-05-07T12:00:00.000Z",
      "events": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block_height` | string | Block height containing events. |
| `block_id` | string | Block ID containing events. |
| `block_timestamp` | date | Block timestamp. |
| `events` | array<object> | Events for the requested type and height range. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /events` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events.md) for the provider-specific parameters and requirements.

