# Create Alert Policy with New Relic

Creates a new alert policy in New Relic.

## Endpoint

- **Method:** `POST`
- **Path:** `/alerts_policies.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Create Alert Policy](https://docs.newrelic.com/docs/alerts/scale-automate/rest-api/rest-api-calls-alerts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Alert policy name. |
| `incident_preference` | body | `list` | yes | How incidents are grouped for this policy. Accepted values: `0`, `1`, `2`. |
