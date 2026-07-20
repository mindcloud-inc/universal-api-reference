# PromptLayer Run Agent: List Prompt Templates

Retrieves prompt templates from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-prompt-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-prompt-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-prompt-templates?${params}`, {
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
| `name` | string | no | Case-insensitive partial match on prompt template name. Example: `wizard-stage3-template-20260424-a`. |
| `label` | string | no | Filter prompt templates by release label. Example: `prod`. |
| `status` | list | no | Filter prompt templates by deletion status: active, deleted, or all. One of: `0`, `1`, `2`. Default: `active`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commitMessage": "string",
      "folderId": 1,
      "fullFolderPath": "string",
      "id": 1,
      "metadata": {},
      "parentFolderName": "Ava Chen",
      "promptName": "Ava Chen",
      "promptTemplate": {},
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
| `folderId` | number |  |
| `fullFolderPath` | string |  |
| `id` | number |  |
| `metadata` | object |  |
| `parentFolderName` | string |  |
| `promptName` | string |  |
| `promptTemplate` | object |  |
| `tags` | array<string> |  |
| `version` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /prompt-templates` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prompt-templates.md) for the provider-specific parameters and requirements.

