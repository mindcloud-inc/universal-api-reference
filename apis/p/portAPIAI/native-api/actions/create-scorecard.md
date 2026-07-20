# Create Scorecard with Port API AI

Creates a scorecard in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/blueprints/:blueprint_identifier/scorecards`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Create Scorecard](https://docs.port.io/api-reference/create-a-scorecard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The Port blueprint identifier. |
| `identifier` | body | `string` | yes | Scorecard identifier |
| `rules[]` | body | `array<object>` | yes | Scorecard rules |
| `title` | body | `string` | yes | Scorecard title |
