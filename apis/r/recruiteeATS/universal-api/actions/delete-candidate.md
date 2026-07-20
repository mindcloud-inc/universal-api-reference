# Recruitee ATS: Delete Candidate



```
DELETE https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/delete-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/delete-candidate?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/delete-candidate?${params}`, {
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
| `id` | number | yes | Candidate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate": {
        "adminappUrl": "https://example.com",
        "adminId": 1,
        "createdAt": "string",
        "deletedAt": "string",
        "deletedByKind": "string",
        "emails": [
          "ava@example.com"
        ],
        "example": true,
        "hasAvatar": true,
        "id": 1,
        "initials": "string",
        "isAnonymous": true,
        "isHired": true,
        "isRevealed": true,
        "lastMessageAt": {},
        "name": "Ava Chen",
        "phones": [
          "string"
        ],
        "photoThumbUrl": "https://example.com",
        "positiveRatings": {},
        "ratingsCount": 1,
        "referrer": {},
        "salutation": {},
        "source": "string",
        "tasksCount": 1,
        "title": {},
        "updatedAt": "string",
        "viewed": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate.adminappUrl` | string |  |
| `candidate.adminId` | number |  |
| `candidate.createdAt` | string |  |
| `candidate.deletedAt` | string |  |
| `candidate.deletedByKind` | string |  |
| `candidate.emails[]` | string |  |
| `candidate.example` | boolean |  |
| `candidate.hasAvatar` | boolean |  |
| `candidate.id` | number |  |
| `candidate.initials` | string |  |
| `candidate.isAnonymous` | boolean |  |
| `candidate.isHired` | boolean |  |
| `candidate.isRevealed` | boolean |  |
| `candidate.lastMessageAt` | object |  |
| `candidate.name` | string |  |
| `candidate.phones[]` | string |  |
| `candidate.photoThumbUrl` | string |  |
| `candidate.positiveRatings` | object |  |
| `candidate.ratingsCount` | number |  |
| `candidate.referrer` | object |  |
| `candidate.salutation` | object |  |
| `candidate.source` | string |  |
| `candidate.tasksCount` | number |  |
| `candidate.title` | object |  |
| `candidate.updatedAt` | string |  |
| `candidate.viewed` | boolean |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `DELETE /c/:company_id/candidates/:id` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-candidate.md) for the provider-specific parameters and requirements.

