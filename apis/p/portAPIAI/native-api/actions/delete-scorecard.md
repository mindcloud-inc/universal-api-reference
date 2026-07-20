# Delete Scorecard with Port API AI

Deletes a scorecard from Port.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/blueprints/:blueprint_identifier/scorecards/:scorecard_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Delete Scorecard](https://docs.port.io/api-reference/delete-a-scorecard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The Port blueprint identifier. |
| `scorecard_identifier` | path | `string` | yes | The Port scorecard identifier. |
