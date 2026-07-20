# OpenFEC: List Committee Totals

Retrieves committee financial totals from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-totals?connectionId=$CONNECTION_ID&limit=25&offset=0&committeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "committeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-totals?${params}`, {
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
      "disbursements": 1,
      "receipts": 1
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
| `disbursements` | number |  |
| `receipts` | number |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /committee/:committee_id/totals/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-committee-totals.md) for the provider-specific parameters and requirements.

