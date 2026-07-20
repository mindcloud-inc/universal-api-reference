# Teach 'n Go: List Students

Retrieves students from Teach 'n Go.

```
GET https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-students
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-students?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-students?${params}`, {
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
      "area": "string",
      "city": "string",
      "classes": [
        {
          "courseFullTitle": "string",
          "courseLevel": "string",
          "courseSubject": "string",
          "courseTitle": "string",
          "enrolmentDate": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "paymentFrequency": "string",
          "recurrence": "string",
          "schoolId": 1,
          "studentId": 1,
          "unenrolmentDate": "2026-05-07T12:00:00.000Z"
        }
      ],
      "countryCode": "string",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "delayedPayments": "string",
      "discountPercentage": "string",
      "discountType": "string",
      "emailAddress": "ava@example.com",
      "flatFloor": "string",
      "fname": "Ava Chen",
      "gender": "string",
      "generalNotes": "string",
      "homePhone": "string",
      "homePhonecode": "string",
      "id": 1,
      "identificationNumber": "string",
      "lname": "Ava Chen",
      "medicalNotes": "string",
      "mobilePhone": "string",
      "mobilePhonecode": "string",
      "numEnrolledCourses": 1,
      "photoLink": "https://example.com",
      "postcode": "string",
      "preferredPaymentMethod": "string",
      "registrationDate": "2026-05-07T12:00:00.000Z",
      "schoolId": 1,
      "streetNameAndNumber": "Ava Chen",
      "wholeAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `area` | string |  |
| `city` | string |  |
| `classes[].courseFullTitle` | string |  |
| `classes[].courseLevel` | string |  |
| `classes[].courseSubject` | string |  |
| `classes[].courseTitle` | string |  |
| `classes[].enrolmentDate` | date |  |
| `classes[].id` | number |  |
| `classes[].paymentFrequency` | string |  |
| `classes[].recurrence` | string |  |
| `classes[].schoolId` | number |  |
| `classes[].studentId` | number |  |
| `classes[].unenrolmentDate` | date |  |
| `countryCode` | string |  |
| `dateOfBirth` | date |  |
| `delayedPayments` | string |  |
| `discountPercentage` | string |  |
| `discountType` | string |  |
| `emailAddress` | string |  |
| `flatFloor` | string |  |
| `fname` | string |  |
| `gender` | string |  |
| `generalNotes` | string |  |
| `homePhone` | string |  |
| `homePhonecode` | string |  |
| `id` | number |  |
| `identificationNumber` | string |  |
| `lname` | string |  |
| `medicalNotes` | string |  |
| `mobilePhone` | string |  |
| `mobilePhonecode` | string |  |
| `numEnrolledCourses` | number |  |
| `photoLink` | string |  |
| `postcode` | string |  |
| `preferredPaymentMethod` | string |  |
| `registrationDate` | date |  |
| `schoolId` | number |  |
| `streetNameAndNumber` | string |  |
| `wholeAddress` | string |  |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /globalApis/student_list` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-students.md) for the provider-specific parameters and requirements.

