# QuintaDB: Update Cell Value

Updates a single cell value in QuintaDB.

```
PUT https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-cell-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-cell-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dtype_id": "string",
  "property_id": "string",
  "val": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-cell-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dtype_id": "string",
    "property_id": "string",
    "val": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dtype_id` | string | yes |  |
| `property_id` | string | yes |  |
| `val` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "new_value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `new_value` | string | New cell value after the update succeeds. |

## Native endpoint

Through the native QuintaDB API, this operation is `PATCH /cell_values/:dtype_id/update_cell_value/:property_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-cell-value.md) for the provider-specific parameters and requirements.

