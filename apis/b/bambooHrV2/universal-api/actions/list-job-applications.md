# BambooHR: List Job Applications

Lists job applications from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-job-applications?${params}`, {
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
| `jobId` | number | no | A Job Id to limit results to |
| `applicationStatusId` | string | no | One or more application status IDs to filter by, comma-separated (e.g. `1,2,3`). Accepts multiple values in one string, delimited by `,`. |
| `applicationStatus` | list<string> | no | One or more application status group codes to filter by, comma-separated (e.g. `NEW,ACTIVE`). Allowed values: `ALL`, `ALL_ACTIVE`, `NEW`, `ACTIVE`, `INACTIVE`, `HIRED`. One of: `ACTIVE`, `ALL`, `ALL_ACTIVE`, `HIRED`, `INACTIVE`, `NEW`. Accepts multiple values in one string, delimited by `,`. |
| `jobStatusGroups` | list<string> | no | One or more position status groups to filter by, comma-separated (e.g. `Draft,Open`). Allowed values: `ALL`, `DRAFT_AND_OPEN`, `Open`, `Filled`, `Draft`, `Deleted`, `On Hold`, `Canceled`. One of: `ALL`, `Canceled`, `DRAFT_AND_OPEN`, `Deleted`, `Draft`, `Filled`, `On Hold`, `Open`. Accepts multiple values in one string, delimited by `,`. |
| `searchString` | string | no | A general search criteria by which to find applications. |
| `sortBy` | list<string> | no | A specific field to sort the results by. One of: `created_date`, `first_name`, `job_title`, `last_updated`, `phone`, `rating`, `status`. |
| `sortOrder` | list<string> | no | Order by which to sort results. One of: `ASC`, `DESC`. |
| `newSince` | date | no | Only return applications submitted after this UTC timestamp. Format: `Y-m-d H:i:s` (e.g. `2024-01-01 13:00:00`). Do NOT use ISO 8601 format (no `T` separator or `Z` suffix). Example: `2024-01-01 13:00:00`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/applicant_tracking/applications` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-applications.md) for the provider-specific parameters and requirements.

