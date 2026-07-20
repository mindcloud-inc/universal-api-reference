# WotNot: Get Knowledge Base Details

Retrieves a knowledge base from WotNot.

```
GET https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-knowledge-base-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-knowledge-base-details?connectionId=$CONNECTION_ID&knowledgeBaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-knowledge-base-details?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_source": [
        {}
      ],
      "domains": [
        {}
      ],
      "id": 1,
      "last_trained_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "ok": true,
      "pagination": {},
      "total_data_sources": 1,
      "total_tokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_source` | array<object> |  |
| `domains` | array<object> |  |
| `id` | number |  |
| `last_trained_at` | date |  |
| `name` | string |  |
| `ok` | boolean |  |
| `pagination` | object |  |
| `total_data_sources` | number |  |
| `total_tokens` | number |  |

## Native endpoint

Through the native WotNot API, this operation is `GET /v1/ai/knowledge-base/:knowledge_base_id` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-details.md) for the provider-specific parameters and requirements.

