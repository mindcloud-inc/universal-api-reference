# HigherGov: List Federal Contracts

Retrieves federal contract awards from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-federal-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-federal-contracts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-federal-contracts?${params}`, {
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
| `awardeeKey` | string | no | HigherGov Awardee Key |
| `awardeeUei` | string | no | Awardee UEI |
| `awardId` | string | no | Government Award ID |
| `awardingAgencyKey` | string | no | HigherGov Awarding Agency key |
| `fundingAgencyKey` | string | no | HigherGov Funding Agency key |
| `lastModifiedDate` | string | no | Last modified date filter in YYYY-MM-DD format |
| `naicsCode` | string | no | Award NAICS code |
| `pscCode` | string | no | Product Service Code |
| `searchId` | string | no | HigherGov SearchID |
| `vehicleKey` | string | no | HigherGov Vehicle key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "award_description_original": "string",
      "award_id": "string",
      "awardee": {},
      "awarding_agency": {},
      "current_total_value_of_award": 1,
      "funding_agency": {},
      "last_modified_date": "string",
      "latest_action_date": "string",
      "parent_award_id": "string",
      "path": "string",
      "total_dollars_obligated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `award_description_original` | string |  |
| `award_id` | string |  |
| `awardee` | object |  |
| `awarding_agency` | object |  |
| `current_total_value_of_award` | number |  |
| `funding_agency` | object |  |
| `last_modified_date` | string |  |
| `latest_action_date` | string |  |
| `parent_award_id` | string |  |
| `path` | string |  |
| `total_dollars_obligated` | number |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/contract/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-federal-contracts.md) for the provider-specific parameters and requirements.

