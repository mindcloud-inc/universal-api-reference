# ClinicalTrials.gov: Search Studies CSV



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/search-studies-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/search-studies-csv?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/search-studies-csv?${params}`, {
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
| `aggFilters` | string | no | Apply aggregate filters using the API's filter syntax. |
| `countTotal` | boolean | no | Include the total number of matching studies. |
| `fields` | string | no | Return only selected fields. |
| `filter.geo` | string | no | Filter results by geographic bounding or distance query. |
| `filter.overallStatus` | string | no | Filter results by study status. |
| `pageSize` | number | no | Number of studies to return. |
| `pageToken` | string | no | Cursor token for the next page. |
| `query.cond` | string | no | Search by condition or disease terms. |
| `query.id` | string | no | Search by NCT ID or other study identifiers. |
| `query.intr` | string | no | Search by intervention or treatment terms. |
| `query.lead` | string | no | Search by lead sponsor terms. |
| `query.locn` | string | no | Search by location terms. |
| `query.outc` | string | no | Search by outcome measure terms. |
| `query.patient` | string | no | Search by patient-facing terms. |
| `query.spons` | string | no | Search by sponsor or collaborator terms. |
| `query.term` | string | no | Search by keyword terms. |
| `query.titles` | string | no | Search by brief title, official title, or acronym. |
| `sort` | string | no | Sort the result set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Raw CSV payload returned by the ClinicalTrials.gov studies search endpoint. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /studies` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-studies-csv.md) for the provider-specific parameters and requirements.

