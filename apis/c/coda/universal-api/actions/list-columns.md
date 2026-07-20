# Coda: List Columns

Retrieves columns from a Coda table.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-columns?connectionId=$CONNECTION_ID&limit=25&offset=0&docId=string&tableIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "docId": "string",
  "tableIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-columns?${params}`, {
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
| `tableIdOrName` | list | yes |  |
| `visibleOnly` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculated": true,
      "display": true,
      "format": {
        "format": "string",
        "isArray": true,
        "type": "string"
      },
      "formula": "string",
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculated` | boolean |  |
| `display` | boolean |  |
| `format.format` | string |  |
| `format.isArray` | boolean |  |
| `format.type` | string |  |
| `formula` | string |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/tables/:tableIdOrName/columns` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-columns.md) for the provider-specific parameters and requirements.

