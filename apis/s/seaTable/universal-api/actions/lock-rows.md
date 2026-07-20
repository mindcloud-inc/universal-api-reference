# SeaTable: Lock Rows

Locks rows in a SeaTable base.

```
PUT https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/lock-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/lock-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/lock-rows', {
  method: 'PUT',
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native SeaTable API, this operation is `PUT /api-gateway/api/v2/dtables/:base_uuid/lock-rows/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lock-rows.md) for the provider-specific parameters and requirements.

