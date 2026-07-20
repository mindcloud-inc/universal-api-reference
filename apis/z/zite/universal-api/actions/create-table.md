# Zite: Create Table

Creates a new table in a Zite database.

```
POST https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zite/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
| `views` | array<object> |  |

## Native endpoint

Through the native Zite API, this operation is `POST /bases/:databaseId/tables` (base URL `https://tables.fillout.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

