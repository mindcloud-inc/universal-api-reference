# Instructure: Get Section

Retrieves a section from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-section?connectionId=$CONNECTION_ID&courseId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-section?${params}`, {
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
| `courseId` | string | yes | Canvas course ID. |
| `id` | string | yes | Canvas section ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "course_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "nonxlist_course_id": "string",
      "sis_section_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `course_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nonxlist_course_id` | string |  |
| `sis_section_id` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /courses/:course_id/sections/:id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-section.md) for the provider-specific parameters and requirements.

