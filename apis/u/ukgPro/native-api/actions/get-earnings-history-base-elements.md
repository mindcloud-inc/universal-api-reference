# Get Earnings History Base Elements with UKG Pro

Payroll earnings history base elements for one pay date (page / per_Page).

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v1/earnings-history-base-elements`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Earnings History Base Elements](https://developer.ukg.com/hcm/reference/earningshistory_getinsrate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payDate` | query | `string` | yes | Pay date, yyyy-MM-dd. UKG spec types it date-time; the legacy job sends yyyy-MM-dd and 60/60 runs returned rows. |
| `companyID` | query | `string` | no | — |
| `employeeID` | query | `string` | no | — |
| `employeeNumber` | query | `string` | no | — |
| `earningCode` | query | `string` | no | — |
| `payGroup` | query | `string` | no | — |
| `periodControl` | query | `string` | no | — |
| `startPerControl` | query | `string` | no | — |
| `endPerControl` | query | `string` | no | — |
| `includeInDeferredCompensation` | query | `boolean` | no | — |
| `includeInDeferredCompensationHours` | query | `boolean` | no | — |
