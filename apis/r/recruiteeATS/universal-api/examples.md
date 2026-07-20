# Recruitee ATS Universal API Examples

These examples use the MindCloud API key and Recruitee ATS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Candidate



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

Example response:

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

See the full [Get Candidate action reference](actions/get-candidate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recruiteeATS/latest/actions/get-candidate).

## Create Candidate



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/create-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "candidate.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/create-candidate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "candidate.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Candidate action reference](actions/create-candidate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recruiteeATS/latest/actions/create-candidate).
