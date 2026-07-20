# Update Risk with ProjectManager

Updates an existing risk in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/risks/:riskId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Update Risk](https://developer.projectmanager.com/api-reference/risk/update-risk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `riskId` | path | `string` | yes | The id of the risk |
| `name` | body | `string` | no | The common name of this Risk. |
| `dueDate` | body | `string` | no | The date when this risk is expected to be resolved. |
| `percentComplete` | body | `string` | no | Percentage completion (0–100). |
| `priority` | body | `string` | no | Priority of the risk. |
| `impact` | body | `string` | no | The potential effect of the risk. |
| `likelihood` | body | `string` | no | Probability of the risk occurring. |
| `responseId` | body | `string` | no | Planned or implemented response. Avoid it, Mitigate, Transfer, Accept |
| `resolution` | body | `string` | no | Actions taken or planned to address the risk. |
| `description` | body | `string` | no | Additional comments or observations. |
| `assignees` | body | `string` | no | Users assigned to the risk. Replaces existing assignments when provided. |
| `tagIds` | body | `string` | no | Tags applied to the risk. Replaces existing tags when provided. |
| `riskTypeId` | body | `string` | no | The type of risk. Risk = 1 Assumption = 2 Issue = 3 Dependency = 4 Change = 5 |
