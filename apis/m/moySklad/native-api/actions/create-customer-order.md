# Create customer order with MoySklad

Creates a customer order in MoySklad.

## Endpoint

- **Method:** `POST`
- **Path:** `entity/customerorder`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Create customer order](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent.meta.href` | body | `string` | yes | MoySklad agent.meta.href argument. |
| `agent.meta.mediaType` | body | `string` | yes | MoySklad agent.meta.mediaType argument. |
| `agent.meta.type` | body | `string` | yes | MoySklad agent.meta.type argument. |
| `name` | body | `string` | yes | MoySklad name argument. |
| `organization.meta.href` | body | `string` | yes | MoySklad organization.meta.href argument. |
| `organization.meta.mediaType` | body | `string` | yes | MoySklad organization.meta.mediaType argument. |
| `organization.meta.type` | body | `string` | yes | MoySklad organization.meta.type argument. |
