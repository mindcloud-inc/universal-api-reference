# OpenFEC: List Committee Reports

Retrieves committee reports from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-reports?connectionId=$CONNECTION_ID&limit=25&offset=0&committeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "committeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-reports?${params}`, {
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
| `committeeId` | string | yes | FEC committee ID, such as C00580100. |
| `cycle` | number | no | Two-year election cycle, such as 2024. Default: `2024`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cash_on_hand_end_period": 1,
      "committee_id": "string",
      "committee_name": "Ava Chen",
      "coverage_end_date": "2026-05-07T12:00:00.000Z",
      "coverage_start_date": "2026-05-07T12:00:00.000Z",
      "cycle": 1,
      "debts_owed_by_committee": 1,
      "report_type": "string",
      "report_type_full": "string",
      "total_disbursements": 1,
      "total_receipts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cash_on_hand_end_period` | number |  |
| `committee_id` | string |  |
| `committee_name` | string |  |
| `coverage_end_date` | date |  |
| `coverage_start_date` | date |  |
| `cycle` | number |  |
| `debts_owed_by_committee` | number |  |
| `report_type` | string |  |
| `report_type_full` | string |  |
| `total_disbursements` | number |  |
| `total_receipts` | number |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /committee/:committee_id/reports/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-committee-reports.md) for the provider-specific parameters and requirements.

