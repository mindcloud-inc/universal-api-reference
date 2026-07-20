# LunaNotes: List Flashcard Quizzes

Retrieves flashcard quizzes from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-flashcard-quizzes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-flashcard-quizzes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-flashcard-quizzes?${params}`, {
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
| `include` | string | no | Comma-separated list of related resources to include. |
| `name` | string | no | Search quizzes by name using a partial match. |
| `sourceType` | string | no | Filter by source type such as video, notes, or ai_agent. |
| `videoId` | string | no | Filter by video ID. |

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

Through the native LunaNotes API, this operation is `GET /v1/flashcard-quizzes` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-flashcard-quizzes.md) for the provider-specific parameters and requirements.

