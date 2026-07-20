# Mentortools: Patch Course Module

Updates part of an existing course module in Mentortools.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course-module" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/patch-course-module', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleId` | number | yes | The module ID. |
| `title` | string | no | Title of the module. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `result` | boolean |  |

## Native endpoint

Through the native Mentortools API, this operation is `PATCH /courses/v1/modules/:module_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-course-module.md) for the provider-specific parameters and requirements.

