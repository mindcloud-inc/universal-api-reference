# HigherGov: List Subgrants

Retrieves subgrant awards from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-subgrants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-subgrants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-subgrants?${params}`, {
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
| `awardingAgencyKey` | string | no | HigherGov Awarding Agency key |
| `fundingAgencyKey` | string | no | HigherGov Funding Agency key |
| `lastModifiedDate` | string | no | Last modified date filter in YYYY-MM-DD format |

## Response

```json
{
  "success": true,
  "data": [
    {
      "last_modified_date": "string",
      "path": "string",
      "prime_grant_award_id": {},
      "sub_awardee": {},
      "sub_awardee_parent": {},
      "subaward_action_date": "string",
      "subaward_amount_total": 1,
      "subaward_description": "string",
      "subaward_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `last_modified_date` | string |  |
| `path` | string |  |
| `prime_grant_award_id` | object |  |
| `sub_awardee` | object |  |
| `sub_awardee_parent` | object |  |
| `subaward_action_date` | string |  |
| `subaward_amount_total` | number |  |
| `subaward_description` | string |  |
| `subaward_id` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/subgrant/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subgrants.md) for the provider-specific parameters and requirements.

