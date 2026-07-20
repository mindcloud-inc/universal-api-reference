# Coda: List Tables

Retrieves tables from a Coda doc.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-tables?connectionId=$CONNECTION_ID&limit=25&offset=0&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-tables?${params}`, {
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
| `docId` | list | yes |  |
| `tableTypes[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserLink": "https://example.com",
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "parent": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "tableType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserLink` | string |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `parent.browserLink` | string |  |
| `parent.href` | string |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.type` | string |  |
| `tableType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/tables` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

