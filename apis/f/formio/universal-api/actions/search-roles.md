# Form.io: Search Roles

Finds roles in Form.io by title pattern.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/search-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/search-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/search-roles?${params}`, {
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
| `limit` | string | no | Maximum number of matching roles to return. |
| `skip` | string | no | Number of matching roles to skip before returning results. |
| `titleRegex` | string | no | Regex filter applied to the role title. |

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

Through the native Form.io API, this operation is `GET /role` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-roles.md) for the provider-specific parameters and requirements.

