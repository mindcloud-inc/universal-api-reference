# Stackoverflow: Undo Question Downvote

Removes a downvote from a question in Stackoverflow.

```
PUT https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/undo-downvote-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/undo-downvote-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/undo-downvote-question', {
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
      "link": "https://example.com",
      "question_id": 1,
      "score": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `question_id` | number |  |
| `score` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `POST /questions/[:id]/downvote/undo` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/undo-downvote-question.md) for the provider-specific parameters and requirements.

