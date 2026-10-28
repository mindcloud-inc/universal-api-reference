# List Employees with UKG Ready

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/companies/:resolvedCid/employees/`
- **Base URL:** `https://{hostname}/ta/rest`
- **Official documentation:** [List Employees](https://secure7.saashr.com/ta/docs/rest/public)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | path | `string` | no | Leave blank to use the company from your connection. Enter a Company ID or !short_name to override it. |
