# SeaTable: Move Rows To Big Data Backend

Moves rows to a SeaTable big data backend.

```
PUT https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/move-rows-to-big-data-backend
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/move-rows-to-big-data-backend" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/move-rows-to-big-data-backend', {
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
      "errorMessage": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SeaTable API, this operation is `POST /api-gateway/api/v2/dtables/:base_uuid/archive-view/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-rows-to-big-data-backend.md) for the provider-specific parameters and requirements.

