# Get My Status Reports with OnePlan

Retrieves your status reports from OnePlan.

## Endpoint

- **Method:** `GET`
- **Path:** `/statusreports/my`
- **Base URL:** `https://my.oneplan.ai/api`
- **Official documentation:** [Get My Status Reports](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-my_States%5B0%5D_States%5B1%5D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `States[0]` | query | `string` | no | Optional first status report state filter from the docs. |
| `States[1]` | query | `string` | no | Optional second status report state filter from the docs. |
