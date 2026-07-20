# Remove Entity From Alert Condition with New Relic

Removes an entity from an alert condition in New Relic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alerts_entity_conditions/:entityId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Remove Entity From Alert Condition](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `condition_id` | query | `number` | yes | Alert condition ID that currently includes the entity. |
| `entity_type` | query | `list` | yes | Entity type: Application, BrowserApplication, MobileApplication, or KeyTransaction. Accepted values: `0`, `1`, `2`, `3`. |
| `entityId` | path | `number` | yes | New Relic alert entity ID. |
