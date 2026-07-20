# Infoplus: Search Low Stock Records

Finds matching low stock records in Infoplus.

```
GET https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-low-stock-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-low-stock-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/search-low-stock-records?${params}`, {
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
      "createDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modifyDate": "2026-05-07T12:00:00.000Z",
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date |  |
| `id` | number |  |
| `modifyDate` | date |  |
| `sku` | string |  |

## Native endpoint

Through the native Infoplus API, this operation is `GET /lowStock/search` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-low-stock-records.md) for the provider-specific parameters and requirements.

