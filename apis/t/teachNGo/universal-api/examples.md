# Teach 'n Go Universal API Examples

These examples use the MindCloud API key and Teach 'n Go connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Students

Retrieves students from Teach 'n Go.

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

Example response:

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

See the full [List Students action reference](actions/list-students.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teachNGo/latest/actions/list-students).

## Add Student Note

Creates a student note in Teach 'n Go.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/add-student-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studentId": "string",
  "visibility": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/add-student-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studentId": "string",
    "visibility": "string",
    "note": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Student Note action reference](actions/add-student-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teachNGo/latest/actions/add-student-note).
