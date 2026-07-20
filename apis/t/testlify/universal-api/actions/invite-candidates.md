# Testlify: Invite Candidates

Creates candidate invitations in Testlify for an assessment.

```
POST https://connect.mindcloud.co/v1/universal/testlify/latest/actions/invite-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/invite-candidates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assessmentId": "string",
  "candidateInvites[].email": "ava@example.com",
  "candidateInvites[].firstName": "Ava",
  "candidateInvites[].lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testlify/latest/actions/invite-candidates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assessmentId": "string",
    "candidateInvites[].email": "ava@example.com",
    "candidateInvites[].firstName": "Ava",
    "candidateInvites[].lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assessmentId` | string | yes | Assessment identifier. |
| `candidateInvites[].email` | string | yes | Candidate email address. |
| `candidateInvites[].firstName` | string | yes | Candidate first name. |
| `candidateInvites[].lastName` | string | yes | Candidate last name. |
| `source` | string | no | Invitation source label. |
| `metadata.correlationId` | string | no | Correlation identifier for downstream tracking. |
| `scheduledDate` | date | no | Scheduled invitation date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidateId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "invitationExpiry": "string",
      "isNotEnoughCredits": true,
      "lastName": "Chen",
      "message": "string",
      "shortLink": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidateId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `invitationExpiry` | string |  |
| `isNotEnoughCredits` | boolean |  |
| `lastName` | string |  |
| `message` | string |  |
| `shortLink` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `POST /v1/assessment/candidate/invites` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-candidates.md) for the provider-specific parameters and requirements.

