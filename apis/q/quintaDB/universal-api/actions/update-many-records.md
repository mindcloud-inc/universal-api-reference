# QuintaDB: Update Many Records

Updates multiple selected records in QuintaDB.

```
PUT https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-many-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-many-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "app_id": "string",
  "confirm_action": "string",
  "entity_id": "string",
  "json_dtype_ids": "string",
  "update_id": "string",
  "update_term": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/update-many-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "app_id": "string",
    "confirm_action": "string",
    "entity_id": "string",
    "json_dtype_ids": "string",
    "update_id": "string",
    "update_term": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `app_id` | string | yes |  |
| `confirm_action` | string | yes |  |
| `entity_id` | string | yes |  |
| `json_dtype_ids` | string | yes |  |
| `update_id` | string | yes |  |
| `update_term` | string | yes |  |
| `view` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string | Bulk update confirmation returned by QuintaDB. |

## Native endpoint

Through the native QuintaDB API, this operation is `POST /dtypes/confirm_action/:app_id/:entity_id.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-many-records.md) for the provider-specific parameters and requirements.

