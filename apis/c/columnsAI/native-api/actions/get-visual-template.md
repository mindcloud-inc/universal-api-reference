# Get Visual Template with Columns AI

Retrieves a visual template from Columns AI by visual ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/snapshot/visual`
- **Base URL:** `https://columns.ai/api`
- **Official documentation:** [Get Visual Template](https://github.com/varchar-io/vaas/blob/main/src/index.ts#L238-L252)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Columns visual ID to load as a template. |
