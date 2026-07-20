# Execute Task with Strale

Executes a task in Strale using semantic matching.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/do`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Execute Task](https://strale.dev/docs#api-do)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dry_run` | body | `boolean` | no | Return the matched capability without executing it. |
| `max_price_cents` | body | `number` | no | Maximum price you are willing to pay in euro cents. |
| `min_sqs` | body | `number` | no | Minimum acceptable Strale Quality Score. |
| `task` | body | `string` | yes | Natural language task to execute. |
| `timeout_seconds` | body | `number` | no | Maximum execution time in seconds. |
