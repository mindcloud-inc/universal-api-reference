# Data Blaze: List Table Fields

Retrieves table fields from Data Blaze.

```
GET https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "primary": true,
      "read_only": true,
      "table_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Data Blaze field ID. |
| `name` | string | Field display name. |
| `primary` | boolean | Whether the field is the primary column. |
| `read_only` | boolean | Whether the field is read-only. |
| `table_id` | string | Owning table ID. |
| `type` | string | Field type. |

## Native endpoint

Through the native Data Blaze API, this operation is `GET /api/database/fields/table/6S69TxVQg3kaNMphZCdHyV/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-fields.md) for the provider-specific parameters and requirements.

