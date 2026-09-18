# List Employees Sensitive Changes with Paycom

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/employee/:eecode/sensitivechange`
- **Base URL:** `https://api.paycomonline.net/v4/rest/index.php/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startdate` | query | `number` | no |
| `enddate` | query | `number` | no |
| `eecode` | path | `string` | no |
