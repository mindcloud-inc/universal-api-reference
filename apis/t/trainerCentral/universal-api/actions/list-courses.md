# TrainerCentral: List Courses

Retrieves courses from TrainerCentral.

```
GET https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-courses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/list-courses?${params}`, {
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
| `filter` | number | no | Optional course source filter. Use 1 for public page, 2 for site builder, 3 for API-created, or 4 for mapped courses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canNonLoginUserAccess": "string",
      "courseId": "string",
      "courseName": "Ava Chen",
      "courseURL": "https://example.com",
      "createdBy": "string",
      "currentUserId": "string",
      "customRegistrationFormId": "string",
      "description": "string",
      "descriptionId": "string",
      "durationType": "string",
      "durationValue": "string",
      "enableReview": "string",
      "enrolledCount": "string",
      "estimatedDurationEnabled": "string",
      "excludeLiveLessonsInCompletion": "string",
      "excludeLiveLessonsInMandation": "string",
      "id": "string",
      "includeAllRecurringTalkInMandation": "string",
      "isFeaturedCourse": "string",
      "isHiddenCourse": "string",
      "isPaidActiveTicketAvailable": "string",
      "isPrivateCourse": "string",
      "isSubsiteCreated": "string",
      "isSubsitePublished": "string",
      "kind": "string",
      "lastUpdatedBy": "string",
      "lastUpdatedTime": "string",
      "links": {
        "assignments": "https://example.com",
        "certificates": "https://example.com",
        "coupons": "https://example.com",
        "drips": "https://example.com",
        "paymentPortals": "https://example.com",
        "reviews": "https://example.com",
        "sections": "https://example.com",
        "sessionInfos": "https://example.com",
        "sessions": "https://example.com",
        "site": "https://example.com",
        "siteSettings": "https://example.com",
        "tests": "https://example.com",
        "tickets": "https://example.com"
      },
      "mandateLessonOrder": "string",
      "materialCompletionEnabled": "string",
      "materialCompletionPercentage": "string",
      "orgId": "string",
      "publishStatus": "string",
      "recordingCompletionEnabled": "string",
      "recordingCompletionPercentage": "string",
      "scheduledTime": "string",
      "scheduleType": "string",
      "subTitle": "string",
      "testCompletionEnabled": "string",
      "time": "string",
      "totalRating": "string",
      "totalRevenue": "string",
      "type": "string",
      "uniqueKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canNonLoginUserAccess` | string |  |
| `courseId` | string |  |
| `courseName` | string |  |
| `courseURL` | string |  |
| `createdBy` | string |  |
| `currentUserId` | string |  |
| `customRegistrationFormId` | string |  |
| `description` | string |  |
| `descriptionId` | string |  |
| `durationType` | string |  |
| `durationValue` | string |  |
| `enableReview` | string |  |
| `enrolledCount` | string |  |
| `estimatedDurationEnabled` | string |  |
| `excludeLiveLessonsInCompletion` | string |  |
| `excludeLiveLessonsInMandation` | string |  |
| `id` | string |  |
| `includeAllRecurringTalkInMandation` | string |  |
| `isFeaturedCourse` | string |  |
| `isHiddenCourse` | string |  |
| `isPaidActiveTicketAvailable` | string |  |
| `isPrivateCourse` | string |  |
| `isSubsiteCreated` | string |  |
| `isSubsitePublished` | string |  |
| `kind` | string |  |
| `lastUpdatedBy` | string |  |
| `lastUpdatedTime` | string |  |
| `links.assignments` | string |  |
| `links.certificates` | string |  |
| `links.coupons` | string |  |
| `links.drips` | string |  |
| `links.paymentPortals` | string |  |
| `links.reviews` | string |  |
| `links.sections` | string |  |
| `links.sessionInfos` | string |  |
| `links.sessions` | string |  |
| `links.site` | string |  |
| `links.siteSettings` | string |  |
| `links.tests` | string |  |
| `links.tickets` | string |  |
| `mandateLessonOrder` | string |  |
| `materialCompletionEnabled` | string |  |
| `materialCompletionPercentage` | string |  |
| `orgId` | string |  |
| `publishStatus` | string |  |
| `recordingCompletionEnabled` | string |  |
| `recordingCompletionPercentage` | string |  |
| `scheduledTime` | string |  |
| `scheduleType` | string |  |
| `subTitle` | string |  |
| `testCompletionEnabled` | string |  |
| `time` | string |  |
| `totalRating` | string |  |
| `totalRevenue` | string |  |
| `type` | string |  |
| `uniqueKey` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `GET /courses.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

