# Mem: Mem It

Creates a note in Mem from raw input.

```
POST https://connect.mindcloud.co/v1/universal/mem/latest/actions/mem-it
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mem/latest/actions/mem-it" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mem/latest/actions/mem-it', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | The raw content to remember. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instructions` | string | no | Optional instructions for how Mem should process the input. |
| `context` | string | no | Optional context to help Mem interpret the input. |
| `timestamp` | date | no | Optional timestamp for the captured memory. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Mem request identifier. |

## Native endpoint

Through the native Mem API, this operation is `POST /v2/mem-it` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mem-it.md) for the provider-specific parameters and requirements.

