# List NRQL Conditions with New Relic

Retrieves NRQL conditions from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts_nrql_conditions.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [List NRQL Conditions](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | query | `number` | yes | Filter NRQL conditions by alert policy ID. |
