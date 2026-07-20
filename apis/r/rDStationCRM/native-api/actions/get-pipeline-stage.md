# Get Pipeline Stage with RD Station CRM

Retrieves a sales pipeline stage from RD Station CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/:pipeline_id/stages/:id`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [Get Pipeline Stage](https://developers.rdstation.com/reference/crm-v2-get-stage-from-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Stage identifier. |
| `pipeline_id` | path | `string` | yes | Pipeline identifier. |
