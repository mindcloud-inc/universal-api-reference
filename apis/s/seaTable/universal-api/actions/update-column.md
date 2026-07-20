# SeaTable: Update Column

Updates a column in a SeaTable base.

```
PUT https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/update-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/update-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/update-column', {
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
      "draggable": true,
      "editable": true,
      "key": "string",
      "name": "Ava Chen",
      "resizable": true,
      "type": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `draggable` | boolean |  |
| `editable` | boolean |  |
| `key` | string |  |
| `name` | string |  |
| `resizable` | boolean |  |
| `type` | string |  |
| `width` | number |  |

## Native endpoint

Through the native SeaTable API, this operation is `PUT /api-gateway/api/v2/dtables/:base_uuid/columns/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-column.md) for the provider-specific parameters and requirements.

