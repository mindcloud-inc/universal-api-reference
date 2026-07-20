# Relevance AI: Get Tool



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-tool?connectionId=$CONNECTION_ID&toolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "toolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-tool?${params}`, {
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
| `toolId` | string | yes | The Relevance AI tool id to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "studio": {
        "description": "string",
        "is_hidden": true,
        "project": "string",
        "public": true,
        "studio_id": "string",
        "title": "string",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `studio.description` | string | The tool description. |
| `studio.is_hidden` | boolean | Whether the tool is hidden. |
| `studio.project` | string | The Relevance AI project ID. |
| `studio.public` | boolean | Whether the tool is public. |
| `studio.studio_id` | string | The tool ID. |
| `studio.title` | string | The tool title. |
| `studio.version` | string | The tool version. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /studios/:toolId/get` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tool.md) for the provider-specific parameters and requirements.

