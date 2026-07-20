# Livestorm: Get Session Person

Retrieves a session person from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-session-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-session-person?connectionId=$CONNECTION_ID&sessionId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-session-person?${params}`, {
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
| `sessionId` | string | yes | Session ID |
| `id` | string | yes | People ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "avatarLink": "https://example.com",
        "createdAt": 1,
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "messagesCount": 1,
        "questionsCount": 1,
        "role": "string",
        "timezone": "string",
        "updatedAt": 1,
        "upVotesCount": 1,
        "votesCount": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.avatarLink` | string |  |
| `attributes.createdAt` | number |  |
| `attributes.email` | string |  |
| `attributes.firstName` | string |  |
| `attributes.lastName` | string |  |
| `attributes.messagesCount` | number |  |
| `attributes.questionsCount` | number |  |
| `attributes.role` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | number |  |
| `attributes.upVotesCount` | number |  |
| `attributes.votesCount` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET sessions/:sessionId/people/:id` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-person.md) for the provider-specific parameters and requirements.

