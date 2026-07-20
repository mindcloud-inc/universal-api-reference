# Print.one Postcards: List Templates

Retrieves templates from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-templates?${params}`, {
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
| `search` | string | no | Search term. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchBy` | string | no | Fields to search by. |
| `labels` | string | no | Deprecated comma-separated labels filter. |
| `formats` | string | no | Deprecated comma-separated formats filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": 1,
      "format": "string",
      "id": "string",
      "labels": [
        "string"
      ],
      "mergeVariables": [
        "string"
      ],
      "name": "Ava Chen",
      "overlay": "string",
      "thumbnail": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | number |  |
| `format` | string |  |
| `id` | string |  |
| `labels[]` | string |  |
| `mergeVariables[]` | string |  |
| `name` | string |  |
| `overlay` | string |  |
| `thumbnail` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/templates` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

