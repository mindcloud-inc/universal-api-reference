# CodeSubmit: Invite Candidate



```
POST https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/invite-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/invite-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/invite-candidate', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dueAt` | string | no | Assessment due date/time |
| `email` | string | no | Candidate email address |
| `firstName` | string | no | Candidate first name |
| `lastName` | string | no | Candidate last name |
| `testId` | string | no | Assessment identifier |
| `timeLimit` | number | no | Time limit in minutes |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate_meta": {},
      "commits_count": 1,
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "last_name": "Chen",
      "status": 1,
      "test": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_meta` | object | Additional candidate metadata. |
| `commits_count` | number | Number of commits recorded for the candidate. |
| `created_at` | string | When the candidate invite was created. |
| `email` | string | Candidate email address. |
| `first_name` | string | Candidate first name. |
| `full_name` | string | Candidate full name. |
| `id` | string | Candidate identifier. |
| `last_name` | string | Candidate last name. |
| `status` | number | Candidate status code. |
| `test` | object | Assessment summary for the invited candidate. |

## Native endpoint

Through the native CodeSubmit API, this operation is `POST /api/external/candidates` (base URL `https://app.codesubmit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-candidate.md) for the provider-specific parameters and requirements.

