# Open AI: Create Response

Creates a model response in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gpt-4o-mini"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/create-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gpt-4o-mini"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input[]` | array<object> | no | Text, image, or file inputs to the model, used to generate a response. |
| `input[].content[].type` | list<string> | no | Example: `input_text`. |
| `input[].role` | list<string> | no |  |
| `input[].content[]` | array<object> | no |  |
| `input[].content[].text` | string | no | Example: `hello!`. |
| `model` | list<string> | yes | ID of the model to use for the response (for example, gpt-4.1 or gpt-4o-mini). Example: `gpt-4o-mini`. |
| `input[].content[].imageUrl` | string | no |  |
| `tools[]` | array<object> | no | Array of objects listing one for each tool |
| `input[].content[].fileUrl` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text.format.type` | list<string> | no |  |
| `text.format` | object | no |  |
| `text` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/responses` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response.md) for the provider-specific parameters and requirements.

