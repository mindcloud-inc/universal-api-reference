# Get Employment Details with UKG Pro

## Endpoint

- **Method:** `GET`
- **Path:** `personnel/v1/employment-details`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Employment Details](https://developer.ukg.com/hcm/reference/get_personnel-v1-employment-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | query | `string` | no | ID of the employee |
| `sort` | query | `list` | no | — |
| `by` | query | `string` | no | — |
| `dateTimeChanged` | query | `string` | no | supports ranges: {01-01-1900,01-01-1901} |
| `primaryJobCode` | query | `string` | no | — |
| `employeeNumber` | query | `string` | no | — |
| `employeeStatusCode` | query | `string` | no | — |
