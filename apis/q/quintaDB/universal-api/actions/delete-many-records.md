# QuintaDB: Delete Many Records

Deletes multiple selected records from QuintaDB.

```
DELETE https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-many-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuintaDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-many-records?connectionId=$CONNECTION_ID&app_id=string&entity_id=string&json_dtype_ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "app_id": "string",
  "entity_id": "string",
  "json_dtype_ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/delete-many-records?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `app_id` | string | yes |  |
| `entity_id` | string | yes |  |
| `json_dtype_ids` | string | yes |  |

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
| `success` | string | Bulk delete confirmation returned by QuintaDB. |

## Native endpoint

Through the native QuintaDB API, this operation is `POST /apps/:app_id/dtypes/delete_multiple.json` (base URL `https://quintadb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-many-records.md) for the provider-specific parameters and requirements.

