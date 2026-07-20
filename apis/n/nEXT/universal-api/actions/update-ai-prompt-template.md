# NEXT: Update AI Prompt Template

Updates an existing AI prompt template in NEXT.

```
PUT https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/update-ai-prompt-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NEXT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/update-ai-prompt-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "prompt": "string",
  "suitable": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/update-ai-prompt-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "prompt": "string",
    "suitable": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The AI prompt template ID. |
| `name` | string | yes | Updated prompt template name. |
| `prompt` | string | yes | Updated prompt instructions. |
| `suitable` | string | yes | Updated highlight scope suitability. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NEXT API returns.

## Native endpoint

Through the native NEXT API, this operation is `PUT /ai-prompt-templates/:id` (base URL `https://rest.eu-west-1.nextapp.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ai-prompt-template.md) for the provider-specific parameters and requirements.

