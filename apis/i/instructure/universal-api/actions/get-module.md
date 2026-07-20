# Instructure: Get Module

Retrieves a module from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-module?connectionId=$CONNECTION_ID&courseId=1&moduleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "1",
  "moduleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-module?${params}`, {
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
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `moduleId` | string | yes | The Canvas module ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "publishFinalGrade": true,
      "requireSequentialProgress": true,
      "unlockAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `position` | number |  |
| `publishFinalGrade` | boolean |  |
| `requireSequentialProgress` | boolean |  |
| `unlockAt` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /courses/:course_id/modules/:module_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-module.md) for the provider-specific parameters and requirements.

