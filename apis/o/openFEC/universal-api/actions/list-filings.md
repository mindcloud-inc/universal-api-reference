# OpenFEC: List Filings

Retrieves a list of filings from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-filings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-filings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-filings?${params}`, {
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
      "candidate_id": "string",
      "committee_id": "string",
      "committee_name": "Ava Chen",
      "coverage_end_date": "2026-05-07T12:00:00.000Z",
      "coverage_start_date": "2026-05-07T12:00:00.000Z",
      "filing_id": 1,
      "form_type": "string",
      "pdf_url": "https://example.com",
      "receipt_date": "2026-05-07T12:00:00.000Z",
      "report_type": "string",
      "report_type_full": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_id` | string |  |
| `committee_id` | string |  |
| `committee_name` | string |  |
| `coverage_end_date` | date |  |
| `coverage_start_date` | date |  |
| `filing_id` | number |  |
| `form_type` | string |  |
| `pdf_url` | string |  |
| `receipt_date` | date |  |
| `report_type` | string |  |
| `report_type_full` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /filings/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-filings.md) for the provider-specific parameters and requirements.

