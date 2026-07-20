# Markup AI: Create Style Rewrite

Creates a style rewrite in Markup AI.

```
POST https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-style-rewrite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-style-rewrite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dialect": "string",
  "styleGuide": "string",
  "fileUpload": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-style-rewrite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dialect": "string",
    "styleGuide": "string",
    "fileUpload": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dialect` | string | yes | The language variant to use for analysis. |
| `tone` | string | no | Optional tone variation to target. |
| `styleGuide` | string | yes | Style guide ID or built-in preset such as ap, chicago, or microsoft. |
| `webhookUrl` | string | no | Optional URL to receive the completed workflow result. |
| `fileUpload` | file | yes | The document to rewrite. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Workflow acceptance status. |
| `workflow_id` | string | Workflow identifier for later status polling. |

## Native endpoint

Through the native Markup AI API, this operation is `POST /v1/style/rewrites` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-style-rewrite.md) for the provider-specific parameters and requirements.

