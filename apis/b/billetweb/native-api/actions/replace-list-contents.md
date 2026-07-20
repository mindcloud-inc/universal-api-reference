# Replace List Contents with Billetweb

Replaces the contents of a Billetweb list.

## Endpoint

- **Method:** `POST`
- **Path:** `/list/:id/replace`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Replace List Contents](https://www.billetweb.fr/bo/api.php#/api/list/:id/replace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Target list identifier. |
| `data[]` | body | `array<array>` | yes | Array of list-entry arrays that will replace existing contents. |
