# NEXT: Create AI Prompt Template

Creates a new AI prompt template in NEXT.

```
POST https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/create-ai-prompt-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NEXT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/create-ai-prompt-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "prompt": "string",
  "suitable": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/create-ai-prompt-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `name` | string | yes | The prompt template name. |
| `prompt` | string | yes | The prompt instructions. |
| `suitable` | string | yes | Which highlight scope this prompt template is suitable for. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NEXT API returns.

## Native endpoint

Through the native NEXT API, this operation is `POST /ai-prompt-templates` (base URL `https://rest.eu-west-1.nextapp.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ai-prompt-template.md) for the provider-specific parameters and requirements.

