# Cross Object Insert with Braintrust

Inserts events and feedback across Braintrust objects.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/insert`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Cross Object Insert](https://braintrust.dev/docs/api-reference/crossobject/cross-object-insert.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_logs` | body | `object` | no | Mapping from project id to project log events and feedback. |
