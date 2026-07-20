# Statistics Netherlands CBS: Get OData V4 Table Properties

Retrieves table properties from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-table-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-table-properties?connectionId=$CONNECTION_ID&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-table-properties?${params}`, {
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
| `tableIdentifier` | string | yes | CBS table identifier, such as 83765NED. |

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
      "TemporalCoverage": "string",
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
| `Description` | string | Table description. |
| `Identifier` | string | Table identifier. |
| `Language` | string | Table language. |
| `Modified` | date | Last modified timestamp. |
| `ObservationCount` | number | Number of observations. |
| `ReleaseDate` | date | Release date. |
| `Status` | string | Dataset status. |
| `TemporalCoverage` | string | Temporal coverage. |
| `Title` | string | Table title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Properties` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-table-properties.md) for the provider-specific parameters and requirements.

