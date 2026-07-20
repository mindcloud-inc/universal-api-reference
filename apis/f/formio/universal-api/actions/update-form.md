# Form.io: Update Form

Updates an existing form in your Form.io project.

```
PUT https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form', {
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
| `display` | string | no | Updated form display mode. |
| `id` | string | yes | The Form.io form ID. |
| `name` | string | no | Updated internal form name. |
| `path` | string | no | Updated public form path slug. |
| `title` | string | no | Updated form title. |
| `type` | string | no | Updated form type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "created": "string",
      "display": "string",
      "machineName": "Ava Chen",
      "modified": "string",
      "name": "Ava Chen",
      "path": "string",
      "project": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `created` | string |  |
| `display` | string |  |
| `machineName` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `path` | string |  |
| `project` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Form.io API, this operation is `PUT /form/:id` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

