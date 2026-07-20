# Update Scorecard with Port API AI

Updates a scorecard in Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/blueprints/:blueprint_identifier/scorecards/:scorecard_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Scorecard](https://docs.port.io/api-reference/change-a-scorecard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The Port blueprint identifier. |
| `identifier` | body | `string` | yes | Scorecard identifier |
| `rules[]` | body | `array<object>` | yes | Scorecard rules |
| `scorecard_identifier` | path | `string` | yes | The Port scorecard identifier. |
| `title` | body | `string` | yes | Scorecard title |
