# GrooveHQ: Search Knowledge Base Categories

Searches knowledge base categories in GrooveHQ.

```
GET https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/search-kb-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/search-kb-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/search-kb-categories?${params}`, {
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
| `keyword` | string | no |  |
| `knowledgeBaseId` | string | no |  |
| `page` | string | no |  |
| `perPage` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrooveHQ API returns.

## Native endpoint

Through the native GrooveHQ API, this operation is `GET /kb/:knowledgeBaseId/categories/search` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-kb-categories.md) for the provider-specific parameters and requirements.

