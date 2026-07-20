# Publish Graph with Columns AI

Publishes a graph to Columns AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/graph`
- **Base URL:** `https://columns.ai/api`
- **Official documentation:** [Publish Graph](https://github.com/varchar-io/vaas/blob/main/src/index.ts#L277-L300)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Tracking ID included in the publish request body. |
| `name` | body | `string` | yes | Name for the published Columns graph. |
| `graph` | body | `object` | yes | Columns GraphData object to publish. |
