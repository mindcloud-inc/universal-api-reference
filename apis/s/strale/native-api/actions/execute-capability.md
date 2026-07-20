# Execute Capability with Strale

Executes a capability in Strale.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/do`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Execute Capability](https://strale.dev/docs#api-do)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capability_slug` | body | `string` | yes | Capability slug to execute directly. |
| `dry_run` | body | `boolean` | no | Return the matched capability without executing it. |
| `inputs` | body | `object` | no | Capability-specific input object. |
| `max_price_cents` | body | `number` | no | Maximum price you are willing to pay in euro cents. |
| `min_sqs` | body | `number` | no | Minimum acceptable Strale Quality Score. |
| `timeout_seconds` | body | `number` | no | Maximum execution time in seconds. |
