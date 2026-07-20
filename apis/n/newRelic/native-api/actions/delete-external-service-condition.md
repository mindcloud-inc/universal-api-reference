# Delete External Service Condition with New Relic

Deletes an existing external service condition from New Relic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alerts_external_service_conditions/:conditionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Delete External Service Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionId` | path | `number` | yes | New Relic alert condition ID. |
