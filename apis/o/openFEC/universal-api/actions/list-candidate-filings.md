# OpenFEC: List Candidate Filings

Retrieves a candidate's filings from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-filings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-filings?connectionId=$CONNECTION_ID&limit=25&offset=0&candidateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "candidateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-filings?${params}`, {
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
| `candidateId` | string | yes | FEC candidate ID, such as P80000722. |

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

Through the native OpenFEC API, this operation is `GET /candidate/:candidate_id/filings/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-candidate-filings.md) for the provider-specific parameters and requirements.

