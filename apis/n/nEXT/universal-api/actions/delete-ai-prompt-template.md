# NEXT: Delete AI Prompt Template

Deletes an existing AI prompt template from NEXT.

```
DELETE https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/delete-ai-prompt-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NEXT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/delete-ai-prompt-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nEXT/latest/actions/delete-ai-prompt-template?${params}`, {
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
| `id` | string | yes | The AI prompt template ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NEXT API returns.

## Native endpoint

Through the native NEXT API, this operation is `DELETE /ai-prompt-templates/:id` (base URL `https://rest.eu-west-1.nextapp.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ai-prompt-template.md) for the provider-specific parameters and requirements.

