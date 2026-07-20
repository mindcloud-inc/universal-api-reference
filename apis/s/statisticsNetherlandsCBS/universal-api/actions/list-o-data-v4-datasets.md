# Statistics Netherlands CBS: List OData V4 Datasets

Retrieves OData V4 datasets from Statistics Netherlands CBS.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-datasets?${params}`, {
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
      "Catalog": "string",
      "DatasetType": "string",
      "Description": "string",
      "Identifier": "string",
      "Language": "string",
      "Modified": "2026-05-07T12:00:00.000Z",
      "ObservationCount": 1,
      "ReleaseDate": "2026-05-07T12:00:00.000Z",
      "Status": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Catalog` | string | Catalog identifier. |
| `DatasetType` | string | Dataset type. |
| `Description` | string | Dataset description. |
| `Identifier` | string | Dataset identifier. |
| `Language` | string | Dataset language. |
| `Modified` | date | Last modified timestamp. |
| `ObservationCount` | number | Number of observations. |
| `ReleaseDate` | date | Release date. |
| `Status` | string | Dataset status. |
| `Title` | string | Dataset title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/Datasets` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-o-data-v4-datasets.md) for the provider-specific parameters and requirements.

