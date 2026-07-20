# Dify: Update Annotation

Updates an existing annotation in Dify.

```
PUT https://connect.mindcloud.co/v1/universal/dify/latest/actions/update-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dify/latest/actions/update-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "annotationId": "string",
  "question": "string",
  "answer": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/update-annotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "annotationId": "string",
    "question": "string",
    "answer": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `annotationId` | string | yes | Annotation ID to update. |
| `question` | string | yes | Updated annotation question. |
| `answer` | string | yes | Updated annotation answer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "createdAt": 1,
      "hitCount": 1,
      "id": "string",
      "question": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `createdAt` | number |  |
| `hitCount` | number |  |
| `id` | string |  |
| `question` | string |  |

## Native endpoint

Through the native Dify API, this operation is `PUT /apps/annotations/:annotation_id` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-annotation.md) for the provider-specific parameters and requirements.

