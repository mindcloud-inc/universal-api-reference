# QuintaDB: Update Record

Updates an existing record in QuintaDB.

```
PUT https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "app_id": "string",
  "dtype_id": "string",
  "json_values": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "app_id": "string",
    "dtype_id": "string",
    "json_values": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `app_id` | string | yes |  |
| `dtype_id` | string | yes |  |
| `json_values` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "record": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `record` | object | Updated QuintaDB record. |

## Native endpoint

Through the native QuintaDB API, this operation is `PUT /apps/:app_id/dtypes/:dtype_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

