# QWIC: Fetch Knowledge Base Details

Retrieves details for a QWIC knowledge base.

```
GET https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/fetch-knowledge-base-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/fetch-knowledge-base-details?connectionId=$CONNECTION_ID&knowledgeBaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeBaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/fetch-knowledge-base-details?${params}`, {
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
| `knowledgeBaseId` | number | yes | The knowledge base ID. |
| `limit` | number | no | The maximum number of data sources to return. |
| `offset` | number | no | The offset for paginated data sources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `GET /v1/ai/knowledge-base/:knowledge_base_id` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-knowledge-base-details.md) for the provider-specific parameters and requirements.

