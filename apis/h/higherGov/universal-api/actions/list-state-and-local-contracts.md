# HigherGov: List State And Local Contracts

Retrieves state and local contract awards from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-state-and-local-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-state-and-local-contracts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-state-and-local-contracts?${params}`, {
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
| `capturedDate` | string | no | Date the award was added to HigherGov |
| `endDate` | string | no | Latest end date for the award in YYYY-MM-DD format |
| `searchId` | string | no | HigherGov SearchID |
| `startDate` | string | no | Earliest start date for the award in YYYY-MM-DD format |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agency_raw": "string",
      "award_amount": "string",
      "awardee_raw": "string",
      "awarding_agency": {},
      "end_date": "string",
      "highergov_key": "string",
      "solicitation_key": "string",
      "source_id": "string",
      "start_date": "string",
      "state_abr": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agency_raw` | string |  |
| `award_amount` | string |  |
| `awardee_raw` | string |  |
| `awarding_agency` | object |  |
| `end_date` | string |  |
| `highergov_key` | string |  |
| `solicitation_key` | string |  |
| `source_id` | string |  |
| `start_date` | string |  |
| `state_abr` | string |  |
| `url` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/sl-contract/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-state-and-local-contracts.md) for the provider-specific parameters and requirements.

