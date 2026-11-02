# BambooHR: List Job Summaries

Lists job summaries from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-summaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-summaries?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statusGroups` | list<string> | no | One or more status groups to filter positions by, comma-separated (e.g. `Draft,Open`). Allowed values: `ALL`, `DRAFT_AND_OPEN`, `Open`, `Filled`, `Draft`, `Deleted`, `On Hold`, `Canceled`. Defaults to all non-deleted positions. One of: `ALL`, `Canceled`, `DRAFT_AND_OPEN`, `Deleted`, `Draft`, `Filled`, `On Hold`, `Open`. Accepts multiple values in one string, delimited by `,`. |
| `statusIds` | string | no | One or more specific job opening status IDs to filter by, comma-separated (e.g. `1,2`). Combined with `statusGroups` when both are provided. Accepts multiple values in one string, delimited by `,`. |
| `sortBy` | list<string> | no | A specific field to sort the results by. One of: `count`, `created`, `lead`, `status`, `title`. |
| `sortOrder` | list<string> | no | Order by which to sort results. One of: `ASC`, `DESC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/applicant_tracking/jobs` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-summaries.md) for the provider-specific parameters and requirements.

