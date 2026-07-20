# Documint: List Templates

Retrieves a list of templates from Documint.

```
GET https://connect.mindcloud.co/v1/universal/documint/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documint/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documint/latest/actions/list-templates?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated list of fields to include in each template record. Example: `name,createdAt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": "string",
      "id": "string",
      "name": "Ava Chen",
      "thumbnail": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | string | Folder identifier or null for the template. |
| `id` | string | Template ID. |
| `name` | string | Template name. |
| `thumbnail` | object | Template thumbnail metadata. |

## Native endpoint

Through the native Documint API, this operation is `GET /templates` (base URL `https://api.documint.me/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

