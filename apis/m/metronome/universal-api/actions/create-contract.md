# Metronome: Create Contract

Creates a new contract in Metronome.

```
POST https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "startingAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-contract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "startingAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The customer ID. |
| `startingAt` | string | yes | Inclusive contract start time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/contracts/create` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract.md) for the provider-specific parameters and requirements.

