# Aspire: List Jobs

Retrieves jobs from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-jobs?${params}`, {
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
      "CancelDate": "2026-05-07T12:00:00.000Z",
      "CanceledByUserID": 1,
      "CanceledFromOpportunity": true,
      "CompleteDate": "2026-05-07T12:00:00.000Z",
      "CompletedUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CustomerJobNum": "string",
      "CustomerPO": "string",
      "JobID": 1,
      "JobStatusID": 1,
      "OpportunityID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CancelDate` | date |  |
| `CanceledByUserID` | number |  |
| `CanceledFromOpportunity` | boolean |  |
| `CompleteDate` | date |  |
| `CompletedUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CustomerJobNum` | string |  |
| `CustomerPO` | string |  |
| `JobID` | number |  |
| `JobStatusID` | number |  |
| `OpportunityID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Jobs` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

