# SeaTable: Duplicate Table

Duplicates a table in a SeaTable base.

```
POST https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/duplicate-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/duplicate-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/duplicate-table', {
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
      "_id": "string",
      "columns": [
        {}
      ],
      "headerSettings": {},
      "idRowMap": {},
      "isHeaderLocked": true,
      "name": "Ava Chen",
      "rows": [
        {}
      ],
      "views": [
        {}
      ],
      "viewStructure": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `columns` | array<object> |  |
| `headerSettings` | object |  |
| `idRowMap` | object |  |
| `isHeaderLocked` | boolean |  |
| `name` | string |  |
| `rows` | array<object> |  |
| `views` | array<object> |  |
| `viewStructure` | object |  |

## Native endpoint

Through the native SeaTable API, this operation is `POST /api-gateway/api/v2/dtables/:base_uuid/tables/duplicate-table/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-table.md) for the provider-specific parameters and requirements.

