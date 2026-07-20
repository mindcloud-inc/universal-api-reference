# Delete NRQL Condition with New Relic

Deletes an existing NRQL condition from New Relic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alerts_nrql_conditions/:conditionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Delete NRQL Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionId` | path | `number` | yes | New Relic alert condition ID. |
