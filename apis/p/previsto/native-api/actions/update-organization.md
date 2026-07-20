# Update Organization with Previsto

Updates an existing organization in Previsto.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:id`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Update Organization](https://developer.previsto.com/organization/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Previsto organization ID. |
| `name` | body | `string` | no | Updated organization name. |
