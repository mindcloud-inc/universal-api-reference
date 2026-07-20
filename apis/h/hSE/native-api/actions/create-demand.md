# Create Demand with 4HSE

Creates a new demand in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/demand/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Demand](https://docs.4hse.com/en/api/demand/#operation-createDemand-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_id` | body | `string` | yes | Action ID. |
| `action_type` | body | `string` | yes | Action type. |
| `resource_id` | body | `string` | yes | Resource ID. |
| `resource_type` | body | `string` | yes | Resource type. |
