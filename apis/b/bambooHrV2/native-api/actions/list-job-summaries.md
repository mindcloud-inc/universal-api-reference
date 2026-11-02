# List Job Summaries with BambooHR

Lists job summaries from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/applicant_tracking/jobs`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Job Summaries](https://documentation.bamboohr.com/reference/get-job-summaries)

## Requirements

- **OAuth scopes:** `hiring:applications`
- **scope:** `hiring:applications` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statusGroups` | query | `list<string>` | no | One or more status groups to filter positions by, comma-separated (e.g. `Draft,Open`). Allowed values: `ALL`, `DRAFT_AND_OPEN`, `Open`, `Filled`, `Draft`, `Deleted`, `On Hold`, `Canceled`. Defaults to all non-deleted positions. Accepted values: `ALL`, `Canceled`, `DRAFT_AND_OPEN`, `Deleted`, `Draft`, `Filled`, `On Hold`, `Open`. Send multiple values as a string separated by `,`. |
| `status_ids` | query | `string` | no | One or more specific job opening status IDs to filter by, comma-separated (e.g. `1,2`). Combined with `statusGroups` when both are provided. Send multiple values as a string separated by `,`. |
| `sortBy` | query | `list<string>` | no | A specific field to sort the results by. Accepted values: `count`, `created`, `lead`, `status`, `title`. |
| `sortOrder` | query | `list<string>` | no | Order by which to sort results. Accepted values: `ASC`, `DESC`. |
