# List Activities with Pipeline CRM

Finds activity notes in Pipeline CRM for a deal, person, or company.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes`
- **Base URL:** `https://api.pipelinecrm.com/api/v3`
- **Official documentation:** [List Activities](https://app.pipelinecrm.com/openapi.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `number` | no | Company association ID. |
| `deal_id` | query | `number` | no | Deal association ID. |
| `person_id` | query | `number` | no | Person association ID. |
