# List SLOs with Datadog

Retrieves service level objectives from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/slo`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List SLOs](https://docs.datadoghq.com/api/latest/service-level-objectives/#get-all-slos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-separated SLO IDs. |
| `query` | query | `string` | no | Filter SLOs by name. |
| `tags_query` | query | `string` | no | Filter SLOs by a tag query. |
| `metrics_query` | query | `string` | no | Filter SLOs by numerator and denominator query. |
| `limit` | query | `number` | no | Maximum number of SLOs to return. |
| `offset` | query | `number` | no | Offset for SLO pagination. |
