# Compare Multiple Platforms with Windsor.ai

Retrieves cross-platform connector data from Windsor.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `https://connectors.windsor.ai/all`
- **Base URL:** `https://onboard.windsor.ai`
- **Official documentation:** [Compare Multiple Platforms](https://windsor.ai/api-documentation/#tab-content42)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_max_rows` | query | `string` | no | Maximum number of rows to return. |
| `date_preset` | query | `string` | no | Relative date window such as last_7d or last_30d. |
| `fields` | query | `string` | yes | Comma-separated list of Windsor.ai fields to retrieve. |
| `filter` | query | `string` | no | JSON filter expression for Windsor.ai connector queries. |
