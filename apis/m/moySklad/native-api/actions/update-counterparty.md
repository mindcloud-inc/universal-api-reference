# Update counterparty with MoySklad

Updates a counterparty in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/counterparty/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update counterparty](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-kontragent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Counterparty update payload. |
| `id` | path | `string` | yes | MoySklad counterparty ID. |
