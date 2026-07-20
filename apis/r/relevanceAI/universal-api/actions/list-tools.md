# Relevance AI: List Tools



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-tools?${params}`, {
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
| `pageSize` | number | no | Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "is_hidden": true,
      "project": "string",
      "public": true,
      "studio_id": "string",
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The tool description. |
| `is_hidden` | boolean | Whether the tool is hidden. |
| `project` | string | The Relevance AI project ID. |
| `public` | boolean | Whether the tool is public. |
| `studio_id` | string | The tool ID. |
| `title` | string | The tool title. |
| `version` | string | The tool version. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /studios/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tools.md) for the provider-specific parameters and requirements.

