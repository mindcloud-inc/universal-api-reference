# List Form Submissions with Jotform

Retrieves submissions for a Jotform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/:id/submissions`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [List Form Submissions](https://api.jotform.com/docs/#form-id-get-form-submissions)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Jotform form ID. |
