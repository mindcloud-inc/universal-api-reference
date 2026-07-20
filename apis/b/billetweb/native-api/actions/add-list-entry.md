# Add List Entry with Billetweb

Adds an entry to a Billetweb list.

## Endpoint

- **Method:** `POST`
- **Path:** `/list/:id/push`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Add List Entry](https://www.billetweb.fr/bo/api.php#/api/list/:id/push)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Target list identifier. |
| `data[]` | body | `array<array>` | yes | Array of list-entry arrays to append. |
