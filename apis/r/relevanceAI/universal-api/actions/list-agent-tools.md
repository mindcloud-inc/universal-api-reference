# Relevance AI: List Agent Tools



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agent-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agent-tools?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-agent-tools?${params}`, {
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
| `agentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_id": "string",
      "description": "string",
      "project": "string",
      "studio_id": "string",
      "title": "string",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_id` | string | The agent action ID. |
| `description` | string | The tool description. |
| `project` | string | The Relevance AI project ID. |
| `studio_id` | string | The tool ID. |
| `title` | string | The tool title. |
| `type` | string | The attached action type. |
| `version` | string | The attached tool version. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /agents/tools/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-tools.md) for the provider-specific parameters and requirements.

