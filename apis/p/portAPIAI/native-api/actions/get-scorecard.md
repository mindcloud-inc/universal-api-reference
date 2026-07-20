# Get Scorecard with Port API AI

Retrieves a scorecard from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/blueprints/:blueprint_identifier/scorecards/:scorecard_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Scorecard](https://docs.port.io/api-reference/get-a-scorecard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | no | The Port blueprint identifier. |
| `scorecard_identifier` | path | `string` | no | The Port scorecard identifier. |
