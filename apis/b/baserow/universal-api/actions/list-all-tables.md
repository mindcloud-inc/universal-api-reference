# Baserow: List All Tables

Retrieves all accessible tables from Baserow.

```
GET https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-all-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-all-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-all-tables?${params}`, {
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
      "databaseId": 1,
      "id": 1,
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `order` | number |  |

## Native endpoint

Through the native Baserow API, this operation is `GET /api/database/tables/all-tables/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-tables.md) for the provider-specific parameters and requirements.

