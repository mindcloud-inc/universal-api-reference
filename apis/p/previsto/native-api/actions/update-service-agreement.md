# Update Service Agreement with Previsto

Updates an existing service agreement in Previsto.

## Endpoint

- **Method:** `PUT`
- **Path:** `/agreements/:id`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Update Service Agreement](https://developer.previsto.com/service-agreements/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Previsto service agreement ID. |
| `description` | body | `string` | no | Updated service agreement description. |
