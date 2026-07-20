# Recruitee ATS: Update Candidate



```
PUT https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/update-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/update-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/update-candidate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Candidate ID. |
| `candidate.name` | string | no | Candidate name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `candidate.remote_cv_url` | string | no | Public URL to the candidate CV file. |
| `candidate.emails` | list<string> | no | Candidate email addresses. |
| `candidate.phones` | list<string> | no | Candidate phone numbers. |
| `candidate.social_links` | list<string> | no | Candidate social profile URLs. |
| `candidate.links` | list<string> | no | Additional candidate links. |
| `candidate.cover_letter` | string | no | Candidate cover letter text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate": {
        "adminappUrl": "https://example.com",
        "adminId": 1,
        "attachmentsCount": 1,
        "coverLetter": {},
        "coverLetterFileOriginalUrl": {},
        "coverLetterFileProcessingStatus": "string",
        "coverLetterFileUrl": {},
        "createdAt": "string",
        "cvOriginalUrl": {},
        "cvParseStatus": {},
        "cvProcessingStatus": "string",
        "cvUrl": {},
        "duplicates": [
          1
        ],
        "emails": [
          "ava@example.com"
        ],
        "eventsCount": 1,
        "example": true,
        "fields": [
          {
            "fixed": true,
            "id": {},
            "isAnonymous": true,
            "kind": "string",
            "origin": "string",
            "visibility": {
              "level": "string"
            },
            "visible": true
          }
        ],
        "followed": true,
        "gdprConsentEverGiven": true,
        "gdprConsentRequestCompletedAt": {},
        "gdprConsentRequestSentAt": {},
        "gdprConsentRequestType": {},
        "gdprExpiresAt": {},
        "gdprScheduledToDeleteAt": {},
        "gdprStatus": "string",
        "hasAvatar": true,
        "hasCoverLetter": true,
        "id": 1,
        "inActiveShare": true,
        "initials": "string",
        "isAnonymous": true,
        "isHired": true,
        "isRevealed": true,
        "lastActivityAt": "string",
        "lastMessageAt": {},
        "mailboxMessagesCount": 1,
        "myLastRating": {},
        "myPendingResultRequest": true,
        "myUpcomingEvent": true,
        "name": "Ava Chen",
        "notesCount": 1,
        "onlineData": {},
        "pendingRequestLink": true,
        "pendingResultRequest": true,
        "phones": [
          "string"
        ],
        "photoThumbUrl": "https://example.com",
        "photoUrl": "https://example.com",
        "positiveRatings": {},
        "ratingsCount": 1,
        "ratingVisible": true,
        "referrer": {},
        "salutation": {},
        "sharedAdminCount": 1,
        "sharedContainerCount": 1,
        "source": "string",
        "sourcingData": {},
        "sourcingOrigin": {},
        "tasksCount": 1,
        "title": {},
        "unreadNotifications": true,
        "upcomingEvent": true,
        "updatedAt": "string",
        "viewed": true
      },
      "references": [
        {
          "anonymizedAt": {},
          "email": "ava@example.com",
          "firstName": "Ava",
          "hasAvatar": true,
          "id": 1,
          "initials": "string",
          "lastName": "Chen",
          "photoNormalUrl": "https://example.com",
          "photoThumbUrl": "https://example.com",
          "timeFormat24": true,
          "timezone": {},
          "type": "string"
        }
      ]
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
| `candidate.attachmentsCount` | number |  |
| `candidate.coverLetter` | object |  |
| `candidate.coverLetterFileOriginalUrl` | object |  |
| `candidate.coverLetterFileProcessingStatus` | string |  |
| `candidate.coverLetterFileUrl` | object |  |
| `candidate.createdAt` | string |  |
| `candidate.cvOriginalUrl` | object |  |
| `candidate.cvParseStatus` | object |  |
| `candidate.cvProcessingStatus` | string |  |
| `candidate.cvUrl` | object |  |
| `candidate.duplicates[]` | number |  |
| `candidate.emails[]` | string |  |
| `candidate.eventsCount` | number |  |
| `candidate.example` | boolean |  |
| `candidate.fields[].fixed` | boolean |  |
| `candidate.fields[].id` | object |  |
| `candidate.fields[].isAnonymous` | boolean |  |
| `candidate.fields[].kind` | string |  |
| `candidate.fields[].origin` | string |  |
| `candidate.fields[].visibility.level` | string |  |
| `candidate.fields[].visible` | boolean |  |
| `candidate.followed` | boolean |  |
| `candidate.gdprConsentEverGiven` | boolean |  |
| `candidate.gdprConsentRequestCompletedAt` | object |  |
| `candidate.gdprConsentRequestSentAt` | object |  |
| `candidate.gdprConsentRequestType` | object |  |
| `candidate.gdprExpiresAt` | object |  |
| `candidate.gdprScheduledToDeleteAt` | object |  |
| `candidate.gdprStatus` | string |  |
| `candidate.hasAvatar` | boolean |  |
| `candidate.hasCoverLetter` | boolean |  |
| `candidate.id` | number |  |
| `candidate.inActiveShare` | boolean |  |
| `candidate.initials` | string |  |
| `candidate.isAnonymous` | boolean |  |
| `candidate.isHired` | boolean |  |
| `candidate.isRevealed` | boolean |  |
| `candidate.lastActivityAt` | string |  |
| `candidate.lastMessageAt` | object |  |
| `candidate.mailboxMessagesCount` | number |  |
| `candidate.myLastRating` | object |  |
| `candidate.myPendingResultRequest` | boolean |  |
| `candidate.myUpcomingEvent` | boolean |  |
| `candidate.name` | string |  |
| `candidate.notesCount` | number |  |
| `candidate.onlineData` | object |  |
| `candidate.pendingRequestLink` | boolean |  |
| `candidate.pendingResultRequest` | boolean |  |
| `candidate.phones[]` | string |  |
| `candidate.photoThumbUrl` | string |  |
| `candidate.photoUrl` | string |  |
| `candidate.positiveRatings` | object |  |
| `candidate.ratingsCount` | number |  |
| `candidate.ratingVisible` | boolean |  |
| `candidate.referrer` | object |  |
| `candidate.salutation` | object |  |
| `candidate.sharedAdminCount` | number |  |
| `candidate.sharedContainerCount` | number |  |
| `candidate.source` | string |  |
| `candidate.sourcingData` | object |  |
| `candidate.sourcingOrigin` | object |  |
| `candidate.tasksCount` | number |  |
| `candidate.title` | object |  |
| `candidate.unreadNotifications` | boolean |  |
| `candidate.upcomingEvent` | boolean |  |
| `candidate.updatedAt` | string |  |
| `candidate.viewed` | boolean |  |
| `references[].anonymizedAt` | object |  |
| `references[].email` | string |  |
| `references[].firstName` | string |  |
| `references[].hasAvatar` | boolean |  |
| `references[].id` | number |  |
| `references[].initials` | string |  |
| `references[].lastName` | string |  |
| `references[].photoNormalUrl` | string |  |
| `references[].photoThumbUrl` | string |  |
| `references[].timeFormat24` | boolean |  |
| `references[].timezone` | object |  |
| `references[].type` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `PATCH /c/:company_id/candidates/:id` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-candidate.md) for the provider-specific parameters and requirements.

