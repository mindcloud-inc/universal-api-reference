# Fillout: Create Table

Creates a new table in Fillout.

```
POST https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "name": "Ava Chen",
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "name": "Ava Chen",
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The database identifier. |
| `name` | string | yes | The table name. |
| `fields[]` | array<object> | yes | The fields to create on the table. |

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

Through the native Fillout API, this operation is `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table.md) for the provider-specific parameters and requirements.

