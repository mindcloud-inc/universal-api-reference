# Create Solution with SmartSuite

Creates a new solution in SmartSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/solutions/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Create Solution](https://developers.smartsuite.com/docs/solution-data/solutions/create-solution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The display name for the new SmartSuite solution. |
| `logo_color` | body | `string` | no | Optional hex color for the solution logo. |
| `logo_icon` | body | `string` | no | Optional SmartSuite icon name for the solution logo. |
