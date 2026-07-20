# Form.io: Get Form

Retrieves a form from your Form.io project.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/get-form?${params}`, {
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
| `id` | string | yes | The Form.io form ID. |

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

Through the native Form.io API, this operation is `GET /form/:id` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

