# OpenFEC: Get Election Summary

Retrieves an election summary from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-election-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-election-summary?connectionId=$CONNECTION_ID&limit=25&offset=0&cycle=1&office=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "cycle": "1",
  "office": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-election-summary?${params}`, {
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
| `cycle` | number | yes | Two-year election cycle, such as 2024. |
| `office` | string | yes | Federal office: president, senate, or house. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate_id": "string",
      "candidate_name": "Ava Chen",
      "cash_on_hand_end_period": 1,
      "cycle": 1,
      "district": "string",
      "office": "string",
      "state": "string",
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
| `candidate_id` | string |  |
| `candidate_name` | string |  |
| `cash_on_hand_end_period` | number |  |
| `cycle` | number |  |
| `district` | string |  |
| `office` | string |  |
| `state` | string |  |
| `total_disbursements` | number |  |
| `total_receipts` | number |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /elections/summary/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-election-summary.md) for the provider-specific parameters and requirements.

