# CustomGPT.ai: Reindex Document

Reindexes a URL-based document in a CustomGPT.ai agent.

```
PUT https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/reindex-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/reindex-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "pageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/reindex-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "pageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID of the agent. |
| `pageId` | number | yes | The document page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updated` | boolean |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `POST /projects/:projectId/pages/:pageId/reindex` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reindex-document.md) for the provider-specific parameters and requirements.

