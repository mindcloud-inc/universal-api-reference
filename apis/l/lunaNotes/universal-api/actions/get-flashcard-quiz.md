# LunaNotes: Get Flashcard Quiz

Retrieves a flashcard quiz from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-flashcard-quiz
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-flashcard-quiz?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-flashcard-quiz?${params}`, {
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
| `id` | string | yes | The LunaNotes flashcard quiz ID. |
| `include` | string | no | Comma-separated: video,flashcards,scores,notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "flashcards": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "scores": [
        {}
      ],
      "sourceType": "string",
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
| `createdAt` | date | Timestamp when the quiz was created |
| `description` | string | Optional quiz description |
| `flashcards` | array<object> | Flashcards in this quiz |
| `id` | string | Unique identifier for the flashcard quiz |
| `name` | string | AI-generated quiz name |
| `notes` | array<object> | Notes linked to this quiz |
| `scores` | array<object> | Quiz attempt scores |
| `sourceType` | string | Quiz source type |
| `updatedAt` | date | Timestamp when the quiz was last updated |
| `userId` | string | Owner user ID |
| `video` | object | Associated video object |
| `videoId` | string | Associated video ID |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/flashcard-quizzes/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flashcard-quiz.md) for the provider-specific parameters and requirements.

