# List embedded templates with MoySklad

Retrieves embedded templates from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/metadata/embeddedtemplate`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List embedded templates](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-shablon-pechatnoi-formy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad document type that supports embedded templates. |
