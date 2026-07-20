# Teach 'n Go: List Courses

Retrieves courses from Teach 'n Go.

```
GET https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-courses?${params}`, {
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
      "archived": true,
      "billingMonthEndDate": "2026-05-07T12:00:00.000Z",
      "billingMonthStartDate": "2026-05-07T12:00:00.000Z",
      "classrooms": "string",
      "color": "string",
      "courseEnded": true,
      "courseFullTitle": "string",
      "courseLevel": "string",
      "courseStarted": true,
      "courseStatus": 1,
      "courseSubject": "string",
      "courseTitle": "string",
      "created": "string",
      "createdBy": 1,
      "customPayments": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isBookingClass": true,
      "isStripeSubAllow": 1,
      "modified": "string",
      "modifiedBy": 1,
      "numEnrolledStudents": 1,
      "paymentFee": "string",
      "paymentFrequency": "string",
      "recurrence": "string",
      "schoolId": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "teacherHourlyFees": "https://example.com",
      "teachers": "string",
      "totalLessons": 1,
      "totalLessonsHrs": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `billingMonthEndDate` | date |  |
| `billingMonthStartDate` | date |  |
| `classrooms` | string |  |
| `color` | string |  |
| `courseEnded` | boolean |  |
| `courseFullTitle` | string |  |
| `courseLevel` | string |  |
| `courseStarted` | boolean |  |
| `courseStatus` | number |  |
| `courseSubject` | string |  |
| `courseTitle` | string |  |
| `created` | string |  |
| `createdBy` | number |  |
| `customPayments` | string |  |
| `endDate` | date |  |
| `id` | number |  |
| `isBookingClass` | boolean |  |
| `isStripeSubAllow` | number |  |
| `modified` | string |  |
| `modifiedBy` | number |  |
| `numEnrolledStudents` | number |  |
| `paymentFee` | string |  |
| `paymentFrequency` | string |  |
| `recurrence` | string |  |
| `schoolId` | number |  |
| `startDate` | date |  |
| `teacherHourlyFees` | string |  |
| `teachers` | string |  |
| `totalLessons` | number |  |
| `totalLessonsHrs` | string |  |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /globalApis/course_list` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

