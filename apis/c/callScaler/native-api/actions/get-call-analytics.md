# Get Call Analytics with CallScaler

Retrieves call analytics from CallScaler.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/calls`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Get Call Analytics](https://callscaler.com/docs/api-analytics)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_flow_id` | query | `string` | no | — |
| `direction` | query | `string` | no | — |
| `end_date` | query | `date` | no | — |
| `group_by` | query | `string` | yes | — |
| `metrics` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `number_id` | query | `string` | no | — |
| `qualified` | query | `boolean` | no | — |
| `source` | query | `string` | no | — |
| `start_date` | query | `date` | no | — |
| `status` | query | `string` | no | — |
