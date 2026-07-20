# Data Blaze: List Table Rows

Retrieves table rows from Data Blaze.

```
GET https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-rows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/list-table-rows?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total number of Mindcloud rows returned by Data Blaze. |
| `next` | string | Pagination URL for the next page when Data Blaze returns more rows. |
| `previous` | string | Pagination URL for the previous page when Data Blaze returns paginated results. |
| `results` | array<object> | List of raw Data Blaze row objects for the Mindcloud table. |

## Native endpoint

Through the native Data Blaze API, this operation is `GET /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-rows.md) for the provider-specific parameters and requirements.

