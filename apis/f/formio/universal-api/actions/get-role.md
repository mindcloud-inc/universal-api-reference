# Form.io: Get Role

Retrieves a role from your Form.io project.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-role?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-role?${params}`, {
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
| `id` | string | yes | The Form.io role ID. |

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

Through the native Form.io API, this operation is `GET /role/:id` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-role.md) for the provider-specific parameters and requirements.

