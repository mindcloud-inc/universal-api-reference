# Dify: Create Annotation

Creates a new annotation in Dify.

```
POST https://connect.mindcloud.co/v1/universal/dify/latest/actions/create-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dify/latest/actions/create-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "question": "string",
  "answer": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/create-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `question` | string | yes | Annotation question. |
| `answer` | string | yes | Annotation answer. |

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

Through the native Dify API, this operation is `POST /apps/annotations` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation.md) for the provider-specific parameters and requirements.

