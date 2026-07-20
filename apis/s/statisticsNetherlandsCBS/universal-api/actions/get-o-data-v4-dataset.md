# Statistics Netherlands CBS: Get OData V4 Dataset

Retrieves an OData V4 dataset from Statistics Netherlands CBS.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dataset?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dataset?${params}`, {
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
| `identifier` | string | yes | CBS OData v4 dataset identifier, such as 00372. |

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

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/Datasets('{{identifier}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-dataset.md) for the provider-specific parameters and requirements.

