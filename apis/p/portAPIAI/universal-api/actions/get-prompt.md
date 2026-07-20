# Port API AI: Get Prompt

Retrieves a prompt from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-prompt?connectionId=$CONNECTION_ID&promptName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promptName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-prompt?${params}`, {
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
| `promptName` | string | yes | The Port MCP prompt name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "prompt": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `prompt` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /mcp/prompts/:prompt_name` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompt.md) for the provider-specific parameters and requirements.

