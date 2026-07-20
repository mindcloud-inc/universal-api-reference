# Edusign: Get Course Timestamps

Retrieves course timestamps from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-timestamps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-timestamps?connectionId=$CONNECTION_ID&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-timestamps?${params}`, {
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
| `courseId` | string | yes | Id of the course |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "course": "string",
          "dateSignature": "string",
          "deviceModel": "string",
          "deviceUuid": "string",
          "fullname": "Ava Chen",
          "geolocation": "string",
          "id": 1,
          "ip": "string",
          "personType": "string",
          "schoolId": "string",
          "signature": "string",
          "studentId": "string",
          "type": 1
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |
| `result[].course` | string |  |
| `result[].dateSignature` | string |  |
| `result[].deviceModel` | string |  |
| `result[].deviceUuid` | string |  |
| `result[].fullname` | string |  |
| `result[].geolocation` | string |  |
| `result[].id` | number |  |
| `result[].ip` | string |  |
| `result[].personType` | string |  |
| `result[].schoolId` | string |  |
| `result[].signature` | string |  |
| `result[].studentId` | string |  |
| `result[].type` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/course/timestamps/:courseId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-timestamps.md) for the provider-specific parameters and requirements.

