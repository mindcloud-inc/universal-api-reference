# Run Structure with Griptape

Runs a structure in Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/structures/:structure_id/runs`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Run Structure](https://docs.griptape.ai/stable/griptape-cloud/structures/run-structure/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `structure_id` | path | `string` | yes | The Griptape structure ID to run. |
| `args[]` | body | `array` | no | Optional positional arguments passed into the Structure Run. |
| `env_vars[]` | body | `array<object>` | no | Optional environment variables to inject into the Structure Run request. |
