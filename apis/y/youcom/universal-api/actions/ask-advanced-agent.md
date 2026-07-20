# You.com: Ask Advanced Agent

Retrieves an advanced agent response from You.com.

```
GET https://connect.mindcloud.co/v1/universal/youcom/latest/actions/ask-advanced-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a You.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/ask-advanced-agent?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/ask-advanced-agent?${params}`, {
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
| `input` | string | yes | Question to answer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": "string",
      "input": [
        [
          {}
        ]
      ],
      "mode": "string",
      "output": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | string | Agent that handled the run. |
| `input[]` | array<object> | Conversation input messages sent to the run. |
| `input[].content` | string | Input message content. |
| `input[].role` | string | Input message role. |
| `mode` | string | Execution mode returned by the API. |
| `output[]` | array<object> | Returned agent output messages. |
| `output[].text` | string | Rendered answer text for the output message. |
| `output[].type` | string | Output message type token. |

## Native endpoint

Through the native You.com API, this operation is `POST /v1/agents/runs` (base URL `https://api.you.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-advanced-agent.md) for the provider-specific parameters and requirements.

