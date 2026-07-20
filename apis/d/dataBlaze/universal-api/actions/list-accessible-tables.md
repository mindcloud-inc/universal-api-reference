# Data Blaze: List Accessible Tables

Retrieves accessible tables from Data Blaze.

```
GET https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-accessible-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-accessible-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-accessible-tables?${params}`, {
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
      "order": 1,
      "space_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Data Blaze table ID. |
| `name` | string | Accessible table name. |
| `order` | number | Table order within the Data Blaze space. |
| `space_id` | string | Owning Data Blaze space ID. |

## Native endpoint

Through the native Data Blaze API, this operation is `GET /api/database/tables/all-tables/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accessible-tables.md) for the provider-specific parameters and requirements.

