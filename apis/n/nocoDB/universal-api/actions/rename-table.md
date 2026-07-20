# NocoDB: Rename Table



```
PUT https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/rename-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/rename-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/rename-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes | Base identifier. |
| `tableId` | string | yes | Table identifier. |
| `title` | string | yes | New title of the table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string",
      "displayFieldId": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "meta": {},
      "sourceId": "string",
      "title": "string",
      "views": [
        {}
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string |  |
| `displayFieldId` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `meta` | object |  |
| `sourceId` | string |  |
| `title` | string |  |
| `views` | array<object> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `PATCH /api/v3/meta/bases/:baseId/tables/:tableId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-table.md) for the provider-specific parameters and requirements.

