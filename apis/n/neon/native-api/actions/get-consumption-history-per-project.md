# Retrieve project consumption metrics (legacy plans) with Neon

Retrieves project consumption metrics from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/consumption_history/projects`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve project consumption metrics (legacy plans)](https://api-docs.neon.tech/reference/getconsumptionhistoryperproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_ids[]` | query | `array<string>` | no | Neon API parameter project_ids Send multiple values as a array. |
| `from` | query | `date` | yes | Neon API parameter from |
| `to` | query | `date` | yes | Neon API parameter to |
| `granularity` | query | `list` | yes | Neon API parameter granularity Accepted values: `0`, `1`, `2`. |
| `org_id` | query | `string` | no | Neon API parameter org_id |
| `include_v1_metrics` | query | `boolean` | no | Neon API parameter include_v1_metrics |
| `metrics[]` | query | `array<string>` | no | Neon API parameter metrics Send multiple values as a array. |
