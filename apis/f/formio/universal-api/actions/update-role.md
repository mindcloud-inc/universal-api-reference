# Form.io: Update Role

Updates an existing role in your Form.io project.

```
PUT https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `admin` | boolean | no | Whether the role is an admin role. |
| `default` | boolean | no | Whether the role is the default role. |
| `description` | string | no | Updated role description. |
| `id` | string | yes | The Form.io role ID. |
| `title` | string | no | Updated role title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "admin": true,
      "created": "string",
      "default": true,
      "description": "string",
      "machineName": "Ava Chen",
      "modified": "string",
      "project": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `admin` | boolean |  |
| `created` | string |  |
| `default` | boolean |  |
| `description` | string |  |
| `machineName` | string |  |
| `modified` | string |  |
| `project` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Form.io API, this operation is `PUT /role/:id` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-role.md) for the provider-specific parameters and requirements.

