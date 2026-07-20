# Delete Synthetics Condition with New Relic

Deletes an existing synthetics condition from New Relic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alerts_synthetics_conditions/:conditionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Delete Synthetics Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionId` | path | `number` | yes | New Relic alert condition ID. |
