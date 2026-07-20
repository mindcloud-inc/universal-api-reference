# HigherGov: List Federal Grants

Retrieves federal grant awards from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-federal-grants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-federal-grants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-federal-grants?${params}`, {
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
| `cfdaProgramNumber` | string | no | Grant Program Number (CFDA) |
| `fundingAgencyKey` | string | no | HigherGov Funding Agency key |
| `lastModifiedDate` | string | no | Last modified date filter in YYYY-MM-DD format |
| `searchId` | string | no | HigherGov SearchID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "award_description_original": "string",
      "award_id": "string",
      "awardee_key": {},
      "awarding_agency": {},
      "federal_action_obligation": 1,
      "funding_agency": {},
      "grant_program": {},
      "last_modified_date": "string",
      "latest_action_date": "string",
      "path": "string",
      "total_obligated_amount": 1
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
| `awardee_key` | object |  |
| `awarding_agency` | object |  |
| `federal_action_obligation` | number |  |
| `funding_agency` | object |  |
| `grant_program` | object |  |
| `last_modified_date` | string |  |
| `latest_action_date` | string |  |
| `path` | string |  |
| `total_obligated_amount` | number |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/grant/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-federal-grants.md) for the provider-specific parameters and requirements.

