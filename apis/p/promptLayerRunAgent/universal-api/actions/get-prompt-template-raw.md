# PromptLayer Run Agent: Get Prompt Template Raw

Retrieves a raw prompt template from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-prompt-template-raw
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-prompt-template-raw?connectionId=$CONNECTION_ID&identifier=wizard-stage3-template-20260424-a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "wizard-stage3-template-20260424-a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-prompt-template-raw?${params}`, {
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
| `identifier` | string | yes | The prompt template name or ID. Example: `wizard-stage3-template-20260424-a`. |
| `resolveSnippets` | boolean | no | Whether to expand snippet references in the returned template. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | number | no | Specific version number to retrieve. |
| `label` | string | no | Release label name to retrieve. Example: `prod`. |
| `includeLlmKwargs` | boolean | no | Whether to include provider-specific llm_kwargs in the response. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commitMessage": "string",
      "createdAt": "string",
      "customProvider": "string",
      "id": 1,
      "llmKwargs": {},
      "metadata": {},
      "promptName": "Ava Chen",
      "promptTemplate": {},
      "providerBaseUrl": "https://example.com",
      "snippets": [
        {}
      ],
      "success": true,
      "tags": [
        "string"
      ],
      "version": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commitMessage` | string |  |
| `createdAt` | string |  |
| `customProvider` | string |  |
| `id` | number |  |
| `llmKwargs` | object |  |
| `metadata` | object |  |
| `promptName` | string |  |
| `promptTemplate` | object |  |
| `providerBaseUrl` | string |  |
| `snippets` | array<object> |  |
| `success` | boolean |  |
| `tags` | array<string> |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /prompt-templates/:identifier` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompt-template-raw.md) for the provider-specific parameters and requirements.

