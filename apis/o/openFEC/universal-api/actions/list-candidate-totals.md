# OpenFEC: List Candidate Totals

Retrieves a candidate's financial totals from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-totals?connectionId=$CONNECTION_ID&limit=25&offset=0&candidateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "candidateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-totals?${params}`, {
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
      "cash_on_hand_end_period": 1,
      "coverage_end_date": "2026-05-07T12:00:00.000Z",
      "coverage_start_date": "2026-05-07T12:00:00.000Z",
      "cycle": 1,
      "debts_owed_by_committee": 1,
      "disbursements": 1,
      "last_report_year": 1,
      "name": "Ava Chen",
      "receipts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_id` | string |  |
| `cash_on_hand_end_period` | number |  |
| `coverage_end_date` | date |  |
| `coverage_start_date` | date |  |
| `cycle` | number |  |
| `debts_owed_by_committee` | number |  |
| `disbursements` | number |  |
| `last_report_year` | number |  |
| `name` | string |  |
| `receipts` | number |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /candidate/:candidate_id/totals/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-candidate-totals.md) for the provider-specific parameters and requirements.

