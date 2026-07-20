# Form.io: Create Form

Creates a new form in your Form.io project.

```
POST https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "path": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "path": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `display` | string | no | Form display mode. Default: `form`. |
| `name` | string | yes | Internal form name. |
| `path` | string | yes | Public form path slug. |
| `title` | string | yes | Human-readable form title. |
| `type` | string | no | Form type such as form or resource. Default: `form`. |

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

Through the native Form.io API, this operation is `POST /form` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

