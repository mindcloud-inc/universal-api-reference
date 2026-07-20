# Nvoip: Create Call



```
POST https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/create-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "called": "string",
  "caller": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "called": "string",
    "caller": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `called` | string | yes | Destino da chamada. |
| `caller` | string | yes | Origem da chamada. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string | Provider call identifier returned after call creation. |
| `state` | string | Provider result state for call creation. |

## Native endpoint

Through the native Nvoip API, this operation is `POST /calls/` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call.md) for the provider-specific parameters and requirements.

