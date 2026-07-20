# Statistics Netherlands CBS: List Tables

Retrieves tables from Statistics Netherlands CBS.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-tables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-tables?${params}`, {
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
      "ApiUrl": "https://example.com",
      "ColumnCount": 1,
      "FeedUrl": "https://example.com",
      "ID": 1,
      "Identifier": "string",
      "Language": "string",
      "RecordCount": 1,
      "ShortTitle": "string",
      "Summary": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ApiUrl` | string | Standard OData API URL. |
| `ColumnCount` | number | Number of table columns. |
| `FeedUrl` | string | OData feed URL. |
| `ID` | number | Catalog table numeric ID. |
| `Identifier` | string | StatLine table identifier. |
| `Language` | string | Catalog language. |
| `RecordCount` | number | Number of table records. |
| `ShortTitle` | string | Short table title. |
| `Summary` | string | Table summary. |
| `Title` | string | Full table title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataCatalog/Tables` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

