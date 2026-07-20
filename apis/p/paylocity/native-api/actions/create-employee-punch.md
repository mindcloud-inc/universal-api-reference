# Create Employee Punch with Paylocity

## Endpoint

- **Method:** `POST`
- **Path:** `apihub/time/v2/companies/:companyId/punchImport`
- **Base URL:** `{connection}`
- **Official documentation:** [Create Employee Punch](https://developer.paylocity.com/integrations/reference/post_apihub_time_v2_companies_companyid_punchimport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[].employeeId` | body | `string` | no | — |
| `data[].lastName` | body | `string` | no | — |
| `data[].firstName` | body | `string` | no | — |
| `data[].date` | body | `string` | no | — |
| `data[].time` | body | `string` | no | — |
| `data[].recordType` | body | `string` | no | Maximum length: 0. |
| `data[].employeeNote` | body | `string` | no | — |
| `data[].supervisorNote` | body | `string` | no | — |
| `data[].payLevel` | body | `string` | no | — |
| `data[].CC1` | body | `string` | no | — |
| `data[].CC2` | body | `string` | no | — |
| `data[].CC3` | body | `string` | no | — |
| `data[].CC4` | body | `string` | no | — |
| `data[].CC5` | body | `string` | no | — |
| `data[].CC6` | body | `string` | no | — |
| `data[].CC7` | body | `string` | no | — |
| `data[].CC8` | body | `string` | no | — |
| `data[].CC9` | body | `string` | no | — |
| `data[].CC10` | body | `string` | no | — |
| `data[].CC11` | body | `string` | no | — |
| `data[].CC12` | body | `string` | no | — |
| `data[].CC13` | body | `string` | no | — |
| `data[].CC14` | body | `string` | no | — |
| `data[].CC15` | body | `string` | no | — |
| `data[].hoursDollars` | body | `string` | no | — |
| `companyId` | path | `string` | yes | — |
| `data[]` | body | `array<object>` | no | — |
