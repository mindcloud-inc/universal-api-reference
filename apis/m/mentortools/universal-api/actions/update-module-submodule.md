# Mentortools: Update Module Submodule

Updates an existing submodule in Mentortools.

```
PUT https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-module-submodule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mentortools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-module-submodule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "submoduleId": 1,
  "order": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/update-module-submodule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "submoduleId": 1,
    "order": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submoduleId` | number | yes | The submodule ID. |
| `order` | number | yes |  |
| `title` | string | yes |  |
| `isPublished` | boolean | no |  |

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

Through the native Mentortools API, this operation is `PUT /courses/v1/submodules/:submodule_id` (base URL `https://app.mentortools.com/public_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-module-submodule.md) for the provider-specific parameters and requirements.

