# List Job Applications with BambooHR

Lists job applications from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/applicant_tracking/applications`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Job Applications](https://documentation.bamboohr.com/reference/get-applications)

## Requirements

- **OAuth scopes:** `hiring:applications`
- **scope:** `hiring:applications` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `number` | no | A Job Id to limit results to |
| `applicationStatusId` | query | `string` | no | One or more application status IDs to filter by, comma-separated (e.g. `1,2,3`). Send multiple values as a string separated by `,`. |
| `applicationStatus` | query | `list<string>` | no | One or more application status group codes to filter by, comma-separated (e.g. `NEW,ACTIVE`). Allowed values: `ALL`, `ALL_ACTIVE`, `NEW`, `ACTIVE`, `INACTIVE`, `HIRED`. Accepted values: `ACTIVE`, `ALL`, `ALL_ACTIVE`, `HIRED`, `INACTIVE`, `NEW`. Send multiple values as a string separated by `,`. |
| `jobStatusGroups` | query | `list<string>` | no | One or more position status groups to filter by, comma-separated (e.g. `Draft,Open`). Allowed values: `ALL`, `DRAFT_AND_OPEN`, `Open`, `Filled`, `Draft`, `Deleted`, `On Hold`, `Canceled`. Accepted values: `ALL`, `Canceled`, `DRAFT_AND_OPEN`, `Deleted`, `Draft`, `Filled`, `On Hold`, `Open`. Send multiple values as a string separated by `,`. |
| `searchString` | query | `string` | no | A general search criteria by which to find applications. |
| `sortBy` | query | `list<string>` | no | A specific field to sort the results by. Accepted values: `created_date`, `first_name`, `job_title`, `last_updated`, `phone`, `rating`, `status`. |
| `sortOrder` | query | `list<string>` | no | Order by which to sort results. Accepted values: `ASC`, `DESC`. |
| `newSince` | query | `date` | no | Only return applications submitted after this UTC timestamp. Format: `Y-m-d H:i:s` (e.g. `2024-01-01 13:00:00`). Do NOT use ISO 8601 format (no `T` separator or `Z` suffix). Format: `YYYY-MM-DD HH:mm:ss`. |
