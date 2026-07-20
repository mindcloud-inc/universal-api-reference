# OpenFEC: Get Itemized Receipt

Retrieves an itemized receipt from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-itemized-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-itemized-receipt?connectionId=$CONNECTION_ID&subId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-itemized-receipt?${params}`, {
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
| `subId` | string | yes | Schedule A transaction sub ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committee_id": "string",
      "committee_name": "Ava Chen",
      "contribution_receipt_amount": 1,
      "contribution_receipt_date": "2026-05-07T12:00:00.000Z",
      "contributor_city": "string",
      "contributor_employer": "string",
      "contributor_name": "Ava Chen",
      "contributor_occupation": "string",
      "contributor_state": "string",
      "memo_text": "string",
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
| `contribution_receipt_amount` | number |  |
| `contribution_receipt_date` | date |  |
| `contributor_city` | string |  |
| `contributor_employer` | string |  |
| `contributor_name` | string |  |
| `contributor_occupation` | string |  |
| `contributor_state` | string |  |
| `memo_text` | string |  |
| `sub_id` | string |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /schedules/schedule_a/:sub_id/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-itemized-receipt.md) for the provider-specific parameters and requirements.

