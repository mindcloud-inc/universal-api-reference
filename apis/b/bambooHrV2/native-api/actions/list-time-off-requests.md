# List Time Off Requests with BambooHR

Lists time off requests from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-off/requests`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Off Requests](https://documentation.bamboohr.com/reference/list-time-off-requests-v1)

## Requirements

- **OAuth scopes:** `time_off:requests`
- **scope:** `time_off:requests` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | OData filter expression applied to time off requests. Supported operators: `eq` (equals, use `eq null` to match NULL), `ne` (not equals, use `ne null` to match NOT NULL), `lt` (less than), `le` (less than or equal), `gt` (greater than), `ge` (greater than or equal), `in` (value in list), `and` (combine clauses). Not supported: `or`, `not`, parenthesized grouping. Filterable fields: `id`, `employeeId`, `categoryId`, `startDate`, `endDate`, `amount`, `unit`, `status`, `requestedAt`. `status` accepts the four values of the response enum. A request that a later edit replaced is never returned by this endpoint, so no filter can select one. Examples: `status eq 'approved'`, `employeeId in (614, 615, 616)`, `status eq 'approved' and startDate ge '2026-04-01' and endDate le '2026-05-01'`. |
| `orderBy` | query | `string` | no | Sort the results by a property and direction, e.g. `requestedAt desc`. Defaults to `requestedAt desc`. |
| `returnActions` | query | `boolean` | no | Set to `true` to include the `_links` block naming the state transitions available to the caller for this time off request. Also accepts `1`, `yes` and `on`. Omitted from the response by default. |
