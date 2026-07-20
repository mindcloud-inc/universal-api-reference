# List Blueprint Scorecards with Port API AI

Retrieves scorecards for a Port blueprint.

## Endpoint

- **Method:** `GET`
- **Path:** `/blueprints/:blueprint_identifier/scorecards`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [List Blueprint Scorecards](https://docs.port.io/api-reference/get-a-blueprints-scorecards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_identifier` | path | `string` | yes | The blueprint identifier. |
