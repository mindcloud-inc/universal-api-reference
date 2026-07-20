# ClinicalTrials.gov: Search Studies



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/search-studies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/search-studies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/search-studies?${params}`, {
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
| `fields` | string | no | Return only selected fields. |
| `filter.geo` | string | no | Filter results by geographic bounding or distance query. |
| `filter.overallStatus` | string | no | Filter results by study status. |
| `pageToken` | string | no | Cursor token for the next page. |
| `query.cond` | string | no | Search within condition fields. |
| `query.id` | string | no | Search by NCT ID or other identifiers. |
| `query.intr` | string | no | Search within intervention fields. |
| `query.lead` | string | no | Search within lead sponsor fields. |
| `query.locn` | string | no | Search by study location text. |
| `query.outc` | string | no | Search within outcome fields. |
| `query.patient` | string | no | Search patient-facing terms. |
| `query.spons` | string | no | Search within sponsor fields. |
| `query.term` | string | no | Search across the default BasicSearch area. |
| `query.titles` | string | no | Search within study title fields. |
| `sort` | string | no | Sort the result set. |
| `countTotal` | boolean | no | Include the total number of matching studies. |
| `pageSize` | number | no | Number of studies to return. |
| `format` | string | no | Response format. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "studies": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string | Cursor token for the next page of studies. |
| `studies` | array<object> | Study records returned for the current page. |
| `totalCount` | number | Total number of matching studies when countTotal is requested. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /studies` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-studies.md) for the provider-specific parameters and requirements.

