# WotNot: Delete Knowledge Base Data Sources

Deletes data sources from a WotNot knowledge base.

```
DELETE https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/delete-knowledge-base-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/delete-knowledge-base-data-sources?connectionId=$CONNECTION_ID&knowledgeBaseId=1&data_sources%5B0%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "1",
  "data_sources[0]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/delete-knowledge-base-data-sources?${params}`, {
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
| `knowledgeBaseId` | number | yes | Knowledge base ID |
| `data_sources[0]` | number | yes | First data source ID to delete |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WotNot API returns.

## Native endpoint

Through the native WotNot API, this operation is `DELETE /v1/ai/knowledge-bases/:knowledge_base_id/data-sources` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-knowledge-base-data-sources.md) for the provider-specific parameters and requirements.

