# Retrieve project consumption metrics with Neon

Retrieves project consumption metrics from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/consumption_history/v2/projects`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve project consumption metrics](https://api-docs.neon.tech/reference/getconsumptionhistoryperprojectv2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_ids[]` | query | `array<string>` | no | Neon API parameter project_ids Send multiple values as a array. |
| `from` | query | `date` | yes | Neon API parameter from |
| `to` | query | `date` | yes | Neon API parameter to |
| `granularity` | query | `list` | yes | Neon API parameter granularity Accepted values: `0`, `1`, `2`. |
| `org_id` | query | `string` | yes | Neon API parameter org_id |
| `metrics[]` | query | `array<string>` | yes | Neon API parameter metrics Send multiple values as a array. |
