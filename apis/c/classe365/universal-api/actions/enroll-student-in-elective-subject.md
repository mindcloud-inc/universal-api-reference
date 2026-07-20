# Classe365: Enroll Student in Elective Subject

Enrolls a student in an elective subject in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/enroll-student-in-elective-subject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/enroll-student-in-elective-subject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/enroll-student-in-elective-subject', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "studentId": 1,
      "subjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `studentId` | number |  |
| `subjectId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/electiveSubjectsAllocation` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-student-in-elective-subject.md) for the provider-specific parameters and requirements.

