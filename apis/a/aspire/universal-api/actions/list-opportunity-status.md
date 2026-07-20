# Aspire: List Opportunity Status

Retrieves opportunity statuses from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-status?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-opportunity-status?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "opportunityStage": "string",
      "opportunityStageName": "Ava Chen",
      "opportunityStatus": "string",
      "opportunityStatusID": 1,
      "opportunityStatusName": "Ava Chen",
      "required": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `opportunityStage` | string |  |
| `opportunityStageName` | string |  |
| `opportunityStatus` | string |  |
| `opportunityStatusID` | number |  |
| `opportunityStatusName` | string |  |
| `required` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `GET OpportunityStatuses` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunity-status.md) for the provider-specific parameters and requirements.

