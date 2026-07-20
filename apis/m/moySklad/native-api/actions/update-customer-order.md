# Update customer order with MoySklad

Updates a customer order in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/customerorder/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update customer order](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent.meta.href` | body | `string` | yes | MoySklad agent.meta.href argument. |
| `agent.meta.mediaType` | body | `string` | yes | MoySklad agent.meta.mediaType argument. |
| `agent.meta.type` | body | `string` | yes | MoySklad agent.meta.type argument. |
| `id` | path | `string` | yes | MoySklad customer order ID. |
| `name` | body | `string` | yes | MoySklad name argument. |
| `organization.meta.href` | body | `string` | yes | MoySklad organization.meta.href argument. |
| `organization.meta.mediaType` | body | `string` | yes | MoySklad organization.meta.mediaType argument. |
| `organization.meta.type` | body | `string` | yes | MoySklad organization.meta.type argument. |
