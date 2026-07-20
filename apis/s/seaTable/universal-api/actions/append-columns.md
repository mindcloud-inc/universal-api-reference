# SeaTable: Append Columns

Creates multiple columns in a SeaTable base.

```
POST https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/append-columns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/append-columns" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/append-columns', {
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
      "columns": [
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
| `columns` | array<object> |  |

## Native endpoint

Through the native SeaTable API, this operation is `POST /api-gateway/api/v2/dtables/:base_uuid/batch-append-columns/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/append-columns.md) for the provider-specific parameters and requirements.

