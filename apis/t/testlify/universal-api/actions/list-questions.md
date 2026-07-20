# Testlify: List Questions

Retrieves Testlify questions with optional filters and pagination.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-questions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-questions?${params}`, {
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
| `query` | string | no | Search query string. |
| `type` | string | no | Question type. |
| `difficulty` | string | no | Question difficulty. |
| `testLibraryId` | string | no | Filter by test library. |
| `isCompanyTestLibraries` | boolean | no | Include company test libraries. |
| `isTestlifyLibraries` | boolean | no | Include Testlify libraries. |
| `language` | string | no | Question language. |
| `isStarred` | boolean | no | Filter starred questions. |
| `isCompanyTest` | boolean | no | Include company test questions. |
| `limit` | number | no | Number of items to return. |
| `skip` | number | no | Number of items to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "codingLanguages": [
        "string"
      ],
      "difficultyLevel": "string",
      "id": "string",
      "isCustomQuestion": true,
      "isStarred": true,
      "language": "string",
      "question": "string",
      "recordingTime": 1,
      "skill": "string",
      "sourceId": 1,
      "testLibraryTitle": "string",
      "timeLimit": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string |  |
| `codingLanguages` | array<string> |  |
| `difficultyLevel` | string |  |
| `id` | string |  |
| `isCustomQuestion` | boolean |  |
| `isStarred` | boolean |  |
| `language` | string |  |
| `question` | string |  |
| `recordingTime` | number |  |
| `skill` | string |  |
| `sourceId` | number |  |
| `testLibraryTitle` | string |  |
| `timeLimit` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/question` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

