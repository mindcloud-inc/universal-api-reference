# PromptLayer Run Agent: Publish Prompt Template

Publishes a prompt template in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/publish-prompt-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/publish-prompt-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "promptTemplate": "[object Object]",
  "promptVersion": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/publish-prompt-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "promptTemplate": "[object Object]",
    "promptVersion": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `promptTemplate` | object | yes | Template registry metadata including prompt_name, tags, and optional folder_id. Example: `[object Object]`. |
| `promptVersion` | object | yes | Prompt version payload including prompt_template content and commit_message. Example: `[object Object]`. |
| `releaseLabels[]` | array<string> | no | Optional release labels to assign to the published version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commitMessage": "string",
      "id": 1,
      "metadata": {},
      "promptName": "Ava Chen",
      "promptTemplate": {},
      "promptVersionId": 1,
      "releaseLabels": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "versionNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commitMessage` | string |  |
| `id` | number |  |
| `metadata` | object |  |
| `promptName` | string |  |
| `promptTemplate` | object |  |
| `promptVersionId` | number |  |
| `releaseLabels` | array<string> |  |
| `tags` | array<string> |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /rest/prompt-templates` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-prompt-template.md) for the provider-specific parameters and requirements.

