# Blaze AI: Generate Doc

Creates an AI-generated document in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/generate-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/generate-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "promptText": "Write a short article about AI workflow automation for operations teams.",
  "generationType": "blog_post",
  "tone": "professional",
  "seoWords": "workflow automation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/generate-doc', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "promptText": "Write a short article about AI workflow automation for operations teams.",
    "generationType": "blog_post",
    "tone": "professional",
    "seoWords": "workflow automation"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Blaze workspace ID. Default: `994619`. |
| `promptText` | string | yes | Prompt text for the new doc. Default: `Write a short article about AI workflow automation for operations teams.`. |
| `generationType` | string | yes | Blaze generation mode. Default: `blog_post`. |
| `tone` | string | yes | Default: `professional`. |
| `seoWords` | string | yes | Default: `workflow automation`. |
| `contentLength` | string | no |  |
| `brandVoiceId` | string | no |  |
| `projectId` | string | no |  |
| `articleId` | string | no |  |
| `title` | string | no | Optional document title. |
| `mode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "folderId": 1,
        "id": 1,
        "key": "string",
        "ownerId": 1,
        "title": "string",
        "updatedAt": "string",
        "workspaceId": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.folderId` | number |  |
| `data.id` | number |  |
| `data.key` | string |  |
| `data.ownerId` | number |  |
| `data.title` | string |  |
| `data.updatedAt` | string |  |
| `data.workspaceId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/docs/ai-generation` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-doc.md) for the provider-specific parameters and requirements.

