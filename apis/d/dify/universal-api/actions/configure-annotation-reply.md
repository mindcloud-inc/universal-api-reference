# Dify: Configure Annotation Reply

Updates annotation reply settings in Dify.

```
PUT https://connect.mindcloud.co/v1/universal/dify/latest/actions/configure-annotation-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dify/latest/actions/configure-annotation-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "embeddingProviderName": "Ava Chen",
  "embeddingModelName": "Ava Chen",
  "scoreThreshold": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/configure-annotation-reply', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "embeddingProviderName": "Ava Chen",
    "embeddingModelName": "Ava Chen",
    "scoreThreshold": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Annotation reply action to configure. |
| `embeddingProviderName` | string | yes | Embedding provider name. |
| `embeddingModelName` | string | yes | Embedding model name. |
| `scoreThreshold` | number | yes | Minimum similarity score threshold. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "jobStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `jobStatus` | string |  |

## Native endpoint

Through the native Dify API, this operation is `POST /apps/annotation-reply/:action` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-annotation-reply.md) for the provider-specific parameters and requirements.

