# Fillout: Update Table

Updates a table in Fillout.

```
PUT https://connect.mindcloud.co/v1/universal/fillout/latest/actions/update-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/update-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillout/latest/actions/update-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The database identifier. |
| `name` | string | no | The updated table name. |
| `tableId` | string | yes | The table identifier. |

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
| `fields` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `order` | number |  |
| `primaryFieldId` | string |  |
| `url` | string |  |
| `views` | array<object> |  |

## Native endpoint

Through the native Fillout API, this operation is `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-table.md) for the provider-specific parameters and requirements.

