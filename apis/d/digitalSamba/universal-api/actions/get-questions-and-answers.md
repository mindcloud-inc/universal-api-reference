# Digital Samba: Get questions and answers

Retrieves room questions and answers from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-questions-and-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-questions-and-answers?connectionId=$CONNECTION_ID&limit=25&offset=0&room=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "room": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-questions-and-answers?${params}`, {
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
| `room` | string | yes | Room path parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | no | UUID of the session. |
| `after` | string | no | The UUID of the question after which records will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "createdAt": "string",
      "externalParticipantId": "string",
      "id": "string",
      "participantId": "string",
      "participantName": "Ava Chen",
      "question": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> |  |
| `createdAt` | string |  |
| `externalParticipantId` | string |  |
| `id` | string |  |
| `participantId` | string |  |
| `participantName` | string |  |
| `question` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /rooms/:room/questions` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-questions-and-answers.md) for the provider-specific parameters and requirements.

