# Get Punch History with Paycom

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/employee/:employeeCode/punchhistory`
- **Base URL:** `https://api.paycomonline.net/v4/rest/index.php/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeCode` | path | `string` | yes |
| `startdate` | query | `date` | no |
| `enddate` | query | `date` | no |
