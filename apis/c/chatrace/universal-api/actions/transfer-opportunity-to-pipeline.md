# Chatrace: Transfer Opportunity To Pipeline

Transfers an opportunity to another Chatrace pipeline.

```
PUT https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/transfer-opportunity-to-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/transfer-opportunity-to-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/transfer-opportunity-to-pipeline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "priority": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `priority` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Chatrace API, this operation is `POST /pipelines/:pipeline_id/opportunities/:opportunity_id/transfer-to-pipeline` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-opportunity-to-pipeline.md) for the provider-specific parameters and requirements.

