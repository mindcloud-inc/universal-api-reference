# Create Metric with HoneyHive

Creates a new metric in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/metrics`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Metric](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Metric name. |
| `task` | body | `string` | yes | Metric task. |
| `type` | body | `string` | yes | Metric type. |
| `description` | body | `string` | yes | Metric description. |
| `return_type` | body | `string` | yes | Metric return type. |
