# Mentortools: Get Course Info

Retrieves detailed course information from Mentortools.

```
GET https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/get-course-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/get-course-info?connectionId=$CONNECTION_ID&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/get-course-info?${params}`, {
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
| `courseId` | number | yes | The course ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "result": {
        "id": 1,
        "isActive": true,
        "order": 1,
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `result.id` | number |  |
| `result.isActive` | boolean |  |
| `result.order` | number |  |
| `result.title` | string |  |

## Native endpoint

Through the native Mentortools API, this operation is `GET /courses/v1/:course_id/info` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-info.md) for the provider-specific parameters and requirements.

