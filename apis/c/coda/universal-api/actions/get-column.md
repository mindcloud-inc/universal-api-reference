# Coda: Get Column

Retrieves column details from a Coda table.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-column?connectionId=$CONNECTION_ID&docId=string&tableIdOrName=Ava%20Chen&columnIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableIdOrName": "Ava Chen",
  "columnIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-column?${params}`, {
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
| `columnIdOrName` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "display": true,
      "format": {
        "isArray": true,
        "type": "string"
      },
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "parent": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "name": "Ava Chen",
        "tableType": "string",
        "type": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display` | boolean |  |
| `format.isArray` | boolean |  |
| `format.type` | string |  |
| `href` | string |  |
| `id` | string |  |
| `name` | string |  |
| `parent.browserLink` | string |  |
| `parent.href` | string |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.tableType` | string |  |
| `parent.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/tables/:tableIdOrName/columns/:columnIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-column.md) for the provider-specific parameters and requirements.

