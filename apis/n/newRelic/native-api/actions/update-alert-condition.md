# Update Alert Condition with New Relic

Updates an existing alert condition in New Relic.

## Endpoint

- **Method:** `PUT`
- **Path:** `/alerts_conditions/:conditionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Update Alert Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionId` | path | `number` | yes | New Relic alert condition ID. |
