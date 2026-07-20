# Update Email with Benchmark Email

Updates an existing email in Benchmark Email.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Emails/:id`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Update Email](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Detail` | body | `object` | yes | Email payload object. |
| `id` | path | `string` | yes | Benchmark email ID. |
