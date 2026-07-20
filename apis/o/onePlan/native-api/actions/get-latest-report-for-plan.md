# Get Latest Report For Plan with OnePlan

Retrieves the latest report for a plan from OnePlan.

## Endpoint

- **Method:** `GET`
- **Path:** `/statusreports/{PlanId}`
- **Base URL:** `https://my.oneplan.ai/api`
- **Official documentation:** [Get Latest Report For Plan](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-PlanId_ReportId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PlanId` | path | `string` | yes | Plan identifier from the path. |
| `ReportId` | query | `string` | no | Optional report identifier query parameter from the docs. |
