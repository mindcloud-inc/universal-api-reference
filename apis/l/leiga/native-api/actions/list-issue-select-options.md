# List Issue Select Options with Leiga

Retrieves selectable issue field options from Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/select-options`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [List Issue Select Options](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741842.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFiledIds[]` | body | `array<number>` | yes | Custom Field IDs |
| `projectId` | body | `number` | yes | Project ID |
