# List External Service Conditions with New Relic

Retrieves external service conditions from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts_external_service_conditions.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [List External Service Conditions](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | query | `number` | yes | Filter external service conditions by alert policy ID. |
