# LunaNotes: Get Flashcard

Retrieves a flashcard from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-flashcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-flashcard?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-flashcard?${params}`, {
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
| `id` | string | yes | The LunaNotes flashcard ID. |
| `include` | string | no | Comma-separated: video. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "options": {},
      "question": "string",
      "quizId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "video": {},
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string | Flashcard answer |
| `createdAt` | date | Creation timestamp |
| `id` | string | Unique identifier for the flashcard |
| `options` | object | Quiz options JSON |
| `question` | string | Flashcard question |
| `quizId` | string | Associated quiz ID |
| `type` | string | Flashcard type |
| `updatedAt` | date | Last update timestamp |
| `userId` | string | Owner user ID |
| `video` | object | Associated video object |
| `videoId` | string | Associated video ID |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/flashcards/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flashcard.md) for the provider-specific parameters and requirements.

