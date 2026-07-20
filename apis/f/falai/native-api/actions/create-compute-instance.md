# Create Compute Instance with fal.ai

Creates a compute instance in fal.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/compute/instances`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Create Compute Instance](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instance_type` | body | `string` | yes | Compute instance type to create. |
| `ssh_key` | body | `string` | yes | SSH public key that will be installed on the new instance. |
