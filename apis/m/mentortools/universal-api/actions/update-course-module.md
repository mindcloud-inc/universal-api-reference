# Mentortools: Update Course Module

Updates an existing course module in Mentortools.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course-module" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleId": 1,
  "title": "string",
  "order": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-course-module', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleId": 1,
    "title": "string",
    "order": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleId` | number | yes | The module ID. |
| `title` | string | yes | Title of the module. |
| `order` | number | yes | Order of the module. |
| `isActive` | boolean | no | Whether the module is active. |
| `isPublished` | boolean | no | Whether the module is published. |
| `mandatory` | boolean | no | Whether the module is mandatory. |

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

Through the native Mentortools API, this operation is `PUT /courses/v1/modules/:module_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-course-module.md) for the provider-specific parameters and requirements.

