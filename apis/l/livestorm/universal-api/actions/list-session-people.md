# Livestorm: List Session People

Retrieves people for a session from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-people?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-people?${params}`, {
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
| `id` | string | yes | Session ID |
| `filter[role]` | string | no | Filter People by role : 'participant', 'team_member' |
| `filter[attended]` | boolean | no | Filter People that attend or not the Session |
| `filter[email]` | string | no | Filter People by their email (exact match) |
| `filter[createdSince]` | date | no | Filter People which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[createdUntil]` | date | no | Filter People which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updatedSince]` | date | no | Filter People which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updatedUntil]` | date | no | Filter People which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `include` | string | no | Include Related Data Accepts multiple values in one string, delimited by `,`. |

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

Through the native Livestorm API, this operation is `GET sessions/:id/people` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-people.md) for the provider-specific parameters and requirements.

