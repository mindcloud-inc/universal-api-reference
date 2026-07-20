# PromptLayer Run Agent: Patch Prompt Template Version

Updates an existing prompt template version in PromptLayer.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/patch-prompt-template-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/patch-prompt-template-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "wizard-stage3-template-20260424-a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/patch-prompt-template-version', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "wizard-stage3-template-20260424-a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | The prompt template name or ID to patch. Example: `wizard-stage3-template-20260424-a`. |
| `messages[]` | array<object> | no | Chat template message patch. Use an array for full replacement or an object keyed by string index for targeted patching. Example: `[object Object],[object Object]`. |
| `commitMessage` | string | no | A message describing the new prompt template version. Example: `Refine summarizer instructions`. |
| `releaseLabels[]` | array<string> | no | Optional release labels to move or assign to the new version. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | number | no | Optional base version number to patch from. Example: `1`. |
| `label` | string | no | Optional release label identifying the base version to patch from. Example: `prod`. |
| `tools[]` | array<object> | no | Optional tools patch for chat templates. |
| `functions[]` | array<object> | no | Optional functions patch for chat templates. |
| `functionCall` | string | no | Optional function_call patch for chat templates. |
| `toolChoice` | string | no | Optional tool_choice patch for chat templates. |
| `content[]` | array<object> | no | Completion template content patch for non-chat templates. |
| `modelParameters` | object | no | Optional model parameter patch. |
| `responseFormat` | object | no | Optional response_format patch. |

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

Through the native PromptLayer Run Agent API, this operation is `PATCH /rest/prompt-templates/:identifier` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-prompt-template-version.md) for the provider-specific parameters and requirements.

