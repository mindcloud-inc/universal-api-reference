# List custom templates with MoySklad

Retrieves custom templates from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/metadata/customtemplate`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List custom templates](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-shablon-pechatnoi-formy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type that supports custom templates. |
