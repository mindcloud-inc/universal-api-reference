# LangChain: Get Session Dashboard



```
GET https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-session-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-session-dashboard?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langChain/latest/actions/get-session-dashboard?${params}`, {
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
| `sessionId` | string | yes | Session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charts": {},
      "description": "string",
      "id": "string",
      "index": 1,
      "session_id": "string",
      "sub_sections": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charts` | object | Top-level chart collection. |
| `description` | string | Dashboard description. |
| `id` | string | Dashboard section UUID. |
| `index` | number | Dashboard section index. |
| `session_id` | string | Session UUID. |
| `sub_sections` | object | Nested dashboard sections and charts. |
| `title` | string | Dashboard title. |

## Native endpoint

Through the native LangChain API, this operation is `POST /api/v1/sessions/:sessionId/dashboard` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-dashboard.md) for the provider-specific parameters and requirements.

