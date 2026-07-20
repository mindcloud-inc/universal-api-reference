# Form.io: List Standard Forms

Retrieves standard forms from your Form.io project.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-standard-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-standard-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-standard-forms?${params}`, {
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
| `limit` | string | no | Maximum number of standard forms to return. |
| `skip` | string | no | Number of standard forms to skip before returning results. |

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

Through the native Form.io API, this operation is `GET /form` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-standard-forms.md) for the provider-specific parameters and requirements.

