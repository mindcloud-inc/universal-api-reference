# TrainerCentral: Create Lesson

Creates a lesson in TrainerCentral.

```
POST https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-lesson
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-lesson" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "session.name": "Ava Chen",
  "session.courseId": "string",
  "session.sectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-lesson', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "session.name": "Ava Chen",
    "session.courseId": "string",
    "session.sectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `session.name` | string | yes | The lesson name. |
| `session.courseId` | string | yes | The course ID the lesson belongs to. |
| `session.sectionId` | string | yes | The chapter ID the lesson belongs to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendedCount": "string",
      "attendeeLimit": "string",
      "course": "string",
      "courseId": "string",
      "createdBy": "string",
      "createdbyName": "Ava Chen",
      "createdTime": "string",
      "deletedTime": "string",
      "deliveryMode": "string",
      "enableDraft": "string",
      "enablePrerequisite": "string",
      "id": "string",
      "invitedCount": "string",
      "joinURL": "https://example.com",
      "links": {
        "assignmentSubmissions": "https://example.com",
        "certificates": "https://example.com",
        "coupons": "https://example.com",
        "evaluation": "https://example.com",
        "mailTemplates": "https://example.com",
        "paymentPortals": "https://example.com",
        "polls": "https://example.com",
        "presentationData": "https://example.com",
        "presentersettings": "https://example.com",
        "recentTalks": "https://example.com",
        "registrationSettings": "https://example.com",
        "remainderTimings": "https://example.com",
        "sessionIntegration": "https://example.com",
        "sessionMaterials": "https://example.com",
        "sessionMaterialSettings": "https://example.com",
        "sessionSettings": "https://example.com",
        "site": "https://example.com",
        "siteSettings": "https://example.com",
        "testAnalytics": "https://example.com",
        "tests": "https://example.com",
        "tickets": "https://example.com"
      },
      "memberRole": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "orgName": "Ava Chen",
      "paymentsHomePageURL": "https://example.com",
      "presenterAutoStartUrl": "https://example.com",
      "presenterUrl": "https://example.com",
      "protoFlag": "string",
      "recurringType": "string",
      "referrer": "string",
      "registeredCount": "string",
      "scheduledBy": "string",
      "scheduledbyName": "Ava Chen",
      "scheduledTime": "string",
      "scheduleType": "string",
      "sessionId": "string",
      "sessionIndex": "string",
      "sessionName": "Ava Chen",
      "sessionScheduledTime": "string",
      "sessionState": "string",
      "sessionType": "string",
      "timezone": "string",
      "timeZone": "string",
      "uniqueKey": "string",
      "zaid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendedCount` | string |  |
| `attendeeLimit` | string |  |
| `course` | string |  |
| `courseId` | string |  |
| `createdBy` | string |  |
| `createdbyName` | string |  |
| `createdTime` | string |  |
| `deletedTime` | string |  |
| `deliveryMode` | string |  |
| `enableDraft` | string |  |
| `enablePrerequisite` | string |  |
| `id` | string |  |
| `invitedCount` | string |  |
| `joinURL` | string |  |
| `links.assignmentSubmissions` | string |  |
| `links.certificates` | string |  |
| `links.coupons` | string |  |
| `links.evaluation` | string |  |
| `links.mailTemplates` | string |  |
| `links.paymentPortals` | string |  |
| `links.polls` | string |  |
| `links.presentationData` | string |  |
| `links.presentersettings` | string |  |
| `links.recentTalks` | string |  |
| `links.registrationSettings` | string |  |
| `links.remainderTimings` | string |  |
| `links.sessionIntegration` | string |  |
| `links.sessionMaterials` | string |  |
| `links.sessionMaterialSettings` | string |  |
| `links.sessionSettings` | string |  |
| `links.site` | string |  |
| `links.siteSettings` | string |  |
| `links.testAnalytics` | string |  |
| `links.tests` | string |  |
| `links.tickets` | string |  |
| `memberRole` | string |  |
| `name` | string |  |
| `orgId` | string |  |
| `orgName` | string |  |
| `paymentsHomePageURL` | string |  |
| `presenterAutoStartUrl` | string |  |
| `presenterUrl` | string |  |
| `protoFlag` | string |  |
| `recurringType` | string |  |
| `referrer` | string |  |
| `registeredCount` | string |  |
| `scheduledBy` | string |  |
| `scheduledbyName` | string |  |
| `scheduledTime` | string |  |
| `scheduleType` | string |  |
| `sessionId` | string |  |
| `sessionIndex` | string |  |
| `sessionName` | string |  |
| `sessionScheduledTime` | string |  |
| `sessionState` | string |  |
| `sessionType` | string |  |
| `timezone` | string |  |
| `timeZone` | string |  |
| `uniqueKey` | string |  |
| `zaid` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `POST /sessions.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lesson.md) for the provider-specific parameters and requirements.

