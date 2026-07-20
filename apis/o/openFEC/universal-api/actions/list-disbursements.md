# OpenFEC: List Disbursements

Retrieves disbursements from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-disbursements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-disbursements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-disbursements?${params}`, {
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
| `committeeId` | string | no | Filter disbursements by FEC committee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committee_id": "string",
      "committee_name": "Ava Chen",
      "disbursement_amount": 1,
      "disbursement_date": "2026-05-07T12:00:00.000Z",
      "disbursement_description": "string",
      "memo_text": "string",
      "recipient_city": "string",
      "recipient_name": "Ava Chen",
      "recipient_state": "string",
      "sub_id": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `committee_id` | string |  |
| `committee_name` | string |  |
| `disbursement_amount` | number |  |
| `disbursement_date` | date |  |
| `disbursement_description` | string |  |
| `memo_text` | string |  |
| `recipient_city` | string |  |
| `recipient_name` | string |  |
| `recipient_state` | string |  |
| `sub_id` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /schedules/schedule_b/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-disbursements.md) for the provider-specific parameters and requirements.

