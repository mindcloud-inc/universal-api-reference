# TrainerCentral: List Upcoming Sessions

Retrieves upcoming live workshops from TrainerCentral.

```
GET https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-upcoming-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-upcoming-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-upcoming-sessions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attendedCount": "string",
      "createdTime": "string",
      "deletedTime": "string",
      "deliveryMode": "string",
      "description": "string",
      "descriptionId": "string",
      "id": "string",
      "invitedCount": "string",
      "isFeaturedLesson": "string",
      "isPaidActiveTicketAvailable": "string",
      "isRepublishNeeded": "string",
      "isSubsiteCreated": "string",
      "isSubsitePublished": "string",
      "joinURL": "https://example.com",
      "kind": "string",
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
      "name": "Ava Chen",
      "orgId": "string",
      "protoFlag": "string",
      "publishStatus": "string",
      "recurringType": "string",
      "referrer": "string",
      "registeredCount": "string",
      "scheduledBy": "string",
      "scheduledEndTime": "string",
      "scheduledTime": "string",
      "scheduleType": "string",
      "sessionId": "string",
      "sessionIndex": "string",
      "sessionType": "string",
      "time": "string",
      "timezone": "string",
      "totalRevenue": "string",
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
| `createdTime` | string |  |
| `deletedTime` | string |  |
| `deliveryMode` | string |  |
| `description` | string |  |
| `descriptionId` | string |  |
| `id` | string |  |
| `invitedCount` | string |  |
| `isFeaturedLesson` | string |  |
| `isPaidActiveTicketAvailable` | string |  |
| `isRepublishNeeded` | string |  |
| `isSubsiteCreated` | string |  |
| `isSubsitePublished` | string |  |
| `joinURL` | string |  |
| `kind` | string |  |
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
| `name` | string |  |
| `orgId` | string |  |
| `protoFlag` | string |  |
| `publishStatus` | string |  |
| `recurringType` | string |  |
| `referrer` | string |  |
| `registeredCount` | string |  |
| `scheduledBy` | string |  |
| `scheduledEndTime` | string |  |
| `scheduledTime` | string |  |
| `scheduleType` | string |  |
| `sessionId` | string |  |
| `sessionIndex` | string |  |
| `sessionType` | string |  |
| `time` | string |  |
| `timezone` | string |  |
| `totalRevenue` | string |  |
| `uniqueKey` | string |  |
| `zaid` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `GET /talks.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-upcoming-sessions.md) for the provider-specific parameters and requirements.

