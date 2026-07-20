# Get Credit Consumption Aggregation with Explorium

Retrieves credit consumption aggregation from Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/credits/aggregation`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Get Credit Consumption Aggregation](https://developers.explorium.ai/reference/credits/get_credit_consumption_aggregation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | body | `string` | yes | Start date and time for the aggregation period in ISO 8601 format. |
| `timezone` | body | `string` | no | Timezone for aggregation boundaries. |
| `to_date` | body | `string` | yes | End date and time for the aggregation period in ISO 8601 format. |
| `mode` | body | `string` | yes | Aggregation mode. |
| `resolution` | body | `string` | yes | Aggregation resolution for timely mode. |
