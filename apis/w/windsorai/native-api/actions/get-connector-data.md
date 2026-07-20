# Get Connector Data with Windsor.ai

Retrieves report data from one Windsor.ai connector.

## Endpoint

- **Method:** `GET`
- **Path:** `https://connectors.windsor.ai/:connector`
- **Base URL:** `https://onboard.windsor.ai`
- **Official documentation:** [Get Connector Data](https://windsor.ai/api-documentation/#tab-content6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_max_rows` | query | `number` | no | Maximum number of rows to return. |
| `connector` | path | `string` | yes | Connector ID such as facebook or googleanalytics4. |
| `date_preset` | query | `string` | no | Relative date window such as last_7d or last_30d. |
| `fields` | query | `string` | yes | Comma-separated list of Windsor.ai fields to retrieve. |
| `filter` | query | `string` | no | JSON filter expression for Windsor.ai connector queries. |
