# Coda: Get Table

Retrieves table details from a Coda doc.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-table?connectionId=$CONNECTION_ID&docId=string&tableIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-table?${params}`, {
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
| `useUpdatedTableLayouts` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserLink": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayColumn": {
        "href": "string",
        "id": "string",
        "type": "string"
      },
      "href": "string",
      "id": "string",
      "layout": "string",
      "name": "Ava Chen",
      "parent": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "rowCount": 1,
      "sorts": [
        {
          "column": {
            "href": "string",
            "id": "string",
            "type": "string"
          },
          "direction": "string"
        }
      ],
      "tableType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "viewId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserLink` | string |  |
| `createdAt` | date |  |
| `displayColumn.href` | string |  |
| `displayColumn.id` | string |  |
| `displayColumn.type` | string |  |
| `href` | string |  |
| `id` | string |  |
| `layout` | string |  |
| `name` | string |  |
| `parent.browserLink` | string |  |
| `parent.href` | string |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.type` | string |  |
| `rowCount` | number |  |
| `sorts[].column.href` | string |  |
| `sorts[].column.id` | string |  |
| `sorts[].column.type` | string |  |
| `sorts[].direction` | string |  |
| `tableType` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `viewId` | string |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/tables/:tableIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table.md) for the provider-specific parameters and requirements.

