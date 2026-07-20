# TrainerCentral: Create Course

Creates a new course in TrainerCentral.

```
POST https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "course.courseName": "Ava Chen",
  "course.subTitle": "string",
  "course.description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "course.courseName": "Ava Chen",
    "course.subTitle": "string",
    "course.description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `course.courseName` | string | yes | The name of the course to create. |
| `course.subTitle` | string | yes | A short subtitle for the course. |
| `course.description` | string | yes | A short course description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "courseId": "string",
      "courseName": "Ava Chen",
      "courseURL": "https://example.com",
      "createdBy": "string",
      "decriptionId": "string",
      "description": "string",
      "enableReview": "string",
      "id": "string",
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
      "orgId": "string",
      "publishStatus": "string",
      "subTitle": "string",
      "time": "string",
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
| `courseId` | string |  |
| `courseName` | string |  |
| `courseURL` | string |  |
| `createdBy` | string |  |
| `decriptionId` | string |  |
| `description` | string |  |
| `enableReview` | string |  |
| `id` | string |  |
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
| `orgId` | string |  |
| `publishStatus` | string |  |
| `subTitle` | string |  |
| `time` | string |  |
| `type` | string |  |
| `uniqueKey` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `POST /courses.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course.md) for the provider-specific parameters and requirements.

