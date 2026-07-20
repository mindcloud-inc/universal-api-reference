# Update Alert Policy with New Relic

Updates an existing alert policy in New Relic.

## Endpoint

- **Method:** `PUT`
- **Path:** `/alerts_policies/:policyId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Update Alert Policy](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | path | `number` | yes | New Relic alert policy ID. |
| `name` | body | `string` | yes | Alert policy name. |
| `incident_preference` | body | `list` | yes | How incidents are grouped for this policy. Accepted values: `0`, `1`, `2`. |
