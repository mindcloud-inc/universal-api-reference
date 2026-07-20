# List Pipeline Stages with RD Station CRM

Retrieves stages from a sales pipeline in RD Station CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/:pipeline_id/stages`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [List Pipeline Stages](https://developers.rdstation.com/reference/crm-v2-list-stages-from-pipeline)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `string` | yes | Pipeline identifier. |
