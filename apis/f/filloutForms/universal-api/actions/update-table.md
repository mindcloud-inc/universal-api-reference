# Fillout Forms: Update Table

Updates an existing table in Fillout.

```
PUT https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "67ef4d500c50cce9",
  "tableId": "t7nUTgYUjzF"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "67ef4d500c50cce9",
    "tableId": "t7nUTgYUjzF"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The unique identifier of the database Example: `67ef4d500c50cce9`. |
| `tableId` | string | yes | The unique identifier of the table. You can also use the table name instead of the ID. Example: `t7nUTgYUjzF`. |
| `name` | string | no | New table name Example: `Leads`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "primaryFieldId": "string",
      "url": "https://example.com",
      "views": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Fields in the table. |
| `id` | string | Table identifier. |
| `name` | string | Table name. |
| `order` | number | Display order of the table. |
| `primaryFieldId` | string | Primary field identifier. |
| `url` | string | Table URL in Fillout. |
| `views` | array<object> | Views in the table. |

## Native endpoint

Through the native Fillout Forms API, this operation is `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-table.md) for the provider-specific parameters and requirements.

