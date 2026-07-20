# Get Metric Data with Reportei

Retrieves metric data from Reportei.

## Endpoint

- **Method:** `POST`
- **Path:** `/metrics/get-data`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Get Metric Data](https://developers.reportei.com#metricas-endpoint-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `date` | yes | Data de início do período. |
| `end` | body | `date` | yes | Data de fim do período. |
| `integration_id` | body | `number` | yes | ID da integração. |
| `metrics[]` | body | `array<object>` | yes | Array de métricas a serem consultadas. |
| `comparison_start` | body | `date` | no | Data de início do período de comparação. |
| `comparison_end` | body | `date` | no | Data de fim do período de comparação. |
