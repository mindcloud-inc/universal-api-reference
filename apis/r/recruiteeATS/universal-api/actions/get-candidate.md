# Recruitee ATS: Get Candidate



```
GET https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/get-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/get-candidate?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/get-candidate?${params}`, {
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
        "adminId": {},
        "attachmentsCount": 1,
        "coverLetter": {},
        "coverLetterFileOriginalUrl": {},
        "coverLetterFileProcessingStatus": "string",
        "coverLetterFileUrl": {},
        "createdAt": "string",
        "cvOriginalUrl": "https://example.com",
        "cvParseStatus": {},
        "cvProcessingStatus": "string",
        "cvUrl": "https://example.com",
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
            "id": 1,
            "isAnonymous": true,
            "kind": "string",
            "origin": "string",
            "values": [
              {
                "languageCode": "string",
                "languageName": "Ava Chen",
                "level": "string"
              }
            ],
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
        "placements": [
          {
            "candidateId": 1,
            "createdAt": "string",
            "departmentId": {},
            "departmentName": {},
            "hiredAt": {},
            "hiredById": {},
            "hiredInOtherPlacement": true,
            "hiredInThisPlacement": true,
            "id": 1,
            "jobStartsAt": {},
            "language": {},
            "locationIds": [
              1
            ],
            "offerId": 1,
            "overdueAt": {},
            "overdueDiff": {},
            "position": 1,
            "positiveRatings": {},
            "ratingVisible": true,
            "stageId": 1,
            "talentPoolId": {},
            "updatedAt": "string"
          }
        ],
        "positiveRatings": {},
        "ratingsCount": 1,
        "ratingVisible": true,
        "referrer": {},
        "salutation": {},
        "sharedAdminCount": 1,
        "sharedContainerCount": 1,
        "source": "string",
        "sources": [
          "string"
        ],
        "sourcingData": {},
        "sourcingOrigin": {},
        "tags": [
          "string"
        ],
        "tasksCount": 1,
        "title": {},
        "unreadNotifications": true,
        "upcomingEvent": true,
        "updatedAt": "string",
        "viewed": true
      },
      "references": [
        {
          "careersJobPageLayoutId": {},
          "createdAt": "string",
          "department": {},
          "departmentId": {},
          "description": "string",
          "guid": "string",
          "highlightHtml": {},
          "hiringManagerId": {},
          "hybrid": true,
          "id": 1,
          "kind": "string",
          "langCode": "string",
          "location": "string",
          "mailboxEmail": "ava@example.com",
          "onSite": true,
          "pipelineTemplateId": 1,
          "position": 1,
          "recruiterId": {},
          "remote": true,
          "requirements": "string",
          "slug": "string",
          "status": "string",
          "title": "string",
          "type": "string",
          "url": "https://example.com",
          "wysiwygEditor": "string"
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
| `candidate.adminId` | object |  |
| `candidate.attachmentsCount` | number |  |
| `candidate.coverLetter` | object |  |
| `candidate.coverLetterFileOriginalUrl` | object |  |
| `candidate.coverLetterFileProcessingStatus` | string |  |
| `candidate.coverLetterFileUrl` | object |  |
| `candidate.createdAt` | string |  |
| `candidate.cvOriginalUrl` | string |  |
| `candidate.cvParseStatus` | object |  |
| `candidate.cvProcessingStatus` | string |  |
| `candidate.cvUrl` | string |  |
| `candidate.duplicates[]` | number |  |
| `candidate.emails[]` | string |  |
| `candidate.eventsCount` | number |  |
| `candidate.example` | boolean |  |
| `candidate.fields[].fixed` | boolean |  |
| `candidate.fields[].id` | number |  |
| `candidate.fields[].isAnonymous` | boolean |  |
| `candidate.fields[].kind` | string |  |
| `candidate.fields[].origin` | string |  |
| `candidate.fields[].values[].languageCode` | string |  |
| `candidate.fields[].values[].languageName` | string |  |
| `candidate.fields[].values[].level` | string |  |
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
| `candidate.placements[].candidateId` | number |  |
| `candidate.placements[].createdAt` | string |  |
| `candidate.placements[].departmentId` | object |  |
| `candidate.placements[].departmentName` | object |  |
| `candidate.placements[].hiredAt` | object |  |
| `candidate.placements[].hiredById` | object |  |
| `candidate.placements[].hiredInOtherPlacement` | boolean |  |
| `candidate.placements[].hiredInThisPlacement` | boolean |  |
| `candidate.placements[].id` | number |  |
| `candidate.placements[].jobStartsAt` | object |  |
| `candidate.placements[].language` | object |  |
| `candidate.placements[].locationIds[]` | number |  |
| `candidate.placements[].offerId` | number |  |
| `candidate.placements[].overdueAt` | object |  |
| `candidate.placements[].overdueDiff` | object |  |
| `candidate.placements[].position` | number |  |
| `candidate.placements[].positiveRatings` | object |  |
| `candidate.placements[].ratingVisible` | boolean |  |
| `candidate.placements[].stageId` | number |  |
| `candidate.placements[].talentPoolId` | object |  |
| `candidate.placements[].updatedAt` | string |  |
| `candidate.positiveRatings` | object |  |
| `candidate.ratingsCount` | number |  |
| `candidate.ratingVisible` | boolean |  |
| `candidate.referrer` | object |  |
| `candidate.salutation` | object |  |
| `candidate.sharedAdminCount` | number |  |
| `candidate.sharedContainerCount` | number |  |
| `candidate.source` | string |  |
| `candidate.sources[]` | string |  |
| `candidate.sourcingData` | object |  |
| `candidate.sourcingOrigin` | object |  |
| `candidate.tags[]` | string |  |
| `candidate.tasksCount` | number |  |
| `candidate.title` | object |  |
| `candidate.unreadNotifications` | boolean |  |
| `candidate.upcomingEvent` | boolean |  |
| `candidate.updatedAt` | string |  |
| `candidate.viewed` | boolean |  |
| `references[].careersJobPageLayoutId` | object |  |
| `references[].createdAt` | string |  |
| `references[].department` | object |  |
| `references[].departmentId` | object |  |
| `references[].description` | string |  |
| `references[].guid` | string |  |
| `references[].highlightHtml` | object |  |
| `references[].hiringManagerId` | object |  |
| `references[].hybrid` | boolean |  |
| `references[].id` | number |  |
| `references[].kind` | string |  |
| `references[].langCode` | string |  |
| `references[].location` | string |  |
| `references[].mailboxEmail` | string |  |
| `references[].onSite` | boolean |  |
| `references[].pipelineTemplateId` | number |  |
| `references[].position` | number |  |
| `references[].recruiterId` | object |  |
| `references[].remote` | boolean |  |
| `references[].requirements` | string |  |
| `references[].slug` | string |  |
| `references[].status` | string |  |
| `references[].title` | string |  |
| `references[].type` | string |  |
| `references[].url` | string |  |
| `references[].wysiwygEditor` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `GET /c/:company_id/candidates/:id` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate.md) for the provider-specific parameters and requirements.

