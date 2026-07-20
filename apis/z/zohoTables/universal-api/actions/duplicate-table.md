# Zoho Tables: Duplicate Table

Creates a duplicate table in Zoho Tables.

```
POST https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/duplicate-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/duplicate-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/duplicate-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes |  |
| `tableId` | string | yes |  |
| `tableName` | string | no |  |
| `isDuplicateWithRecords` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldsCount": 1,
      "name": "Ava Chen",
      "recordsCount": 1,
      "tableId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldsCount` | number | Number of fields in the table. |
| `name` | string | Table name. |
| `recordsCount` | number | Number of records in the table. |
| `tableId` | string | Zoho table identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `POST /tables` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-table.md) for the provider-specific parameters and requirements.

