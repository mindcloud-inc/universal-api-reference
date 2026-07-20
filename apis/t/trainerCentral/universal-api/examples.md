# TrainerCentral Universal API Examples

These examples use the MindCloud API key and TrainerCentral connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Courses

Retrieves courses from TrainerCentral.

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

Example response:

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

See the full [List Courses action reference](actions/list-courses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trainerCentral/latest/actions/list-courses).

## Create Chapter

Creates a new chapter in TrainerCentral.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-chapter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "section.courseId": "string",
  "section.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-chapter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "section.courseId": "string",
    "section.name": "Ava Chen"
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
      "createdBy": "string",
      "createdTime": "string",
      "id": "string",
      "lastUpdatedBy": "string",
      "lastUpdatedTime": "string",
      "sectionId": "string",
      "sectionIndex": "string",
      "sectionName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Chapter action reference](actions/create-chapter.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trainerCentral/latest/actions/create-chapter).
