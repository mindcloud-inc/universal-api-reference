# PromptLayer Run Agent: Get Prompt Template

Retrieves a prompt template from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-prompt-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-prompt-template?connectionId=$CONNECTION_ID&identifier=wizard-stage3-template-20260424-a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "wizard-stage3-template-20260424-a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-prompt-template?${params}`, {
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
| `inputVariables` | object | no | Optional input variables used to render the prompt template. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | number | no | Optional version number to retrieve. Example: `1`. |
| `workspaceId` | number | no | Optional workspace override. |
| `label` | string | no | Optional release label to retrieve. Example: `prod`. |
| `provider` | list | no | Optional provider used for default llm_kwargs resolution. One of: `0`, `1`. |
| `metadataFilters` | object | no | Optional metadata filters used for A/B label selection. |
| `model` | string | no | Optional model name used to return default llm_kwargs. |
| `modelParameterOverrides` | object | no | Optional provider-specific model parameter overrides. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commitMessage": "string",
      "customProvider": "string",
      "id": 1,
      "llmKwargs": {},
      "metadata": {},
      "promptName": "Ava Chen",
      "promptTemplate": {},
      "providerBaseUrl": "https://example.com",
      "providerId": 1,
      "requestId": "string",
      "snippets": [
        {}
      ],
      "tags": [
        "string"
      ],
      "version": 1,
      "warning": "string",
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
| `customProvider` | string |  |
| `id` | number |  |
| `llmKwargs` | object |  |
| `metadata` | object |  |
| `promptName` | string |  |
| `promptTemplate` | object |  |
| `providerBaseUrl` | string |  |
| `providerId` | number |  |
| `requestId` | string |  |
| `snippets` | array<object> |  |
| `tags` | array<string> |  |
| `version` | number |  |
| `warning` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /prompt-templates/:identifier` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompt-template.md) for the provider-specific parameters and requirements.

