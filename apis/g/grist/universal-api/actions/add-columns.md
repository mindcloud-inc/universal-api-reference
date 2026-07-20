# Grist: Add Columns

Creates new columns in a Grist table.

```
POST https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-columns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "tableId": "string",
  "columns": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grist/latest/actions/add-columns', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "tableId": "string",
    "columns": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document ID |
| `tableId` | list<string> | yes | Table ID (e.g. Table1) |
| `columns` | string | yes | Array of {id: 'ColName', fields: {type: 'Text', label: 'Column Label'}} |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns[].id` | string |  |

## Native endpoint

Through the native Grist API, this operation is `POST /docs/:docId/tables/:tableId/columns` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-columns.md) for the provider-specific parameters and requirements.

