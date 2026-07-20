# SeaTable: Move Rows To Normal Backend

Moves rows back to a SeaTable normal backend.

```
PUT https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/move-rows-to-normal-backend
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/move-rows-to-normal-backend" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/move-rows-to-normal-backend', {
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
      "success": true,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `taskId` | string |  |

## Native endpoint

Through the native SeaTable API, this operation is `POST /api-gateway/api/v2/dtables/:base_uuid/unarchive/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-rows-to-normal-backend.md) for the provider-specific parameters and requirements.

