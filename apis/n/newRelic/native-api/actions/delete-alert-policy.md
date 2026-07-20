# Delete Alert Policy with New Relic

Deletes an existing alert policy from New Relic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/alerts_policies/:policyId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Delete Alert Policy](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | path | `number` | yes | New Relic alert policy ID. |
