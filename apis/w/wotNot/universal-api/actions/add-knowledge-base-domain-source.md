# WotNot: Add Knowledge Base Domain Source

Adds a domain source to a WotNot knowledge base.

```
PUT https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/add-knowledge-base-domain-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/add-knowledge-base-domain-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/add-knowledge-base-domain-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgeBaseId": 1,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `knowledgeBaseId` | number | yes | Knowledge base ID |
| `url` | string | yes | Domain URL to crawl |
| `excludeUrls` | string | no | Optional URLs to exclude |
| `refreshFrequency` | string | no | Optional refresh frequency |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain_id": 1,
      "ok": true,
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain_id` | number |  |
| `ok` | boolean |  |
| `request_id` | string |  |

## Native endpoint

Through the native WotNot API, this operation is `POST /v1/ai/knowledge-base/:knowledge_base_id/data-sources/domain` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-knowledge-base-domain-source.md) for the provider-specific parameters and requirements.

