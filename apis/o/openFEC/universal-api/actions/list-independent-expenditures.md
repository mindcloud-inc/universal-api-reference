# OpenFEC: List Independent Expenditures

Retrieves independent expenditures from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-independent-expenditures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-independent-expenditures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-independent-expenditures?${params}`, {
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
| `candidateId` | string | no | Filter independent expenditures by FEC candidate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate_id": "string",
      "candidate_name": "Ava Chen",
      "committee_id": "string",
      "committee_name": "Ava Chen",
      "expenditure_amount": 1,
      "expenditure_date": "2026-05-07T12:00:00.000Z",
      "payee_name": "Ava Chen",
      "sub_id": "string",
      "support_oppose_indicator": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_id` | string |  |
| `candidate_name` | string |  |
| `committee_id` | string |  |
| `committee_name` | string |  |
| `expenditure_amount` | number |  |
| `expenditure_date` | date |  |
| `payee_name` | string |  |
| `sub_id` | string |  |
| `support_oppose_indicator` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /schedules/schedule_e/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-independent-expenditures.md) for the provider-specific parameters and requirements.

