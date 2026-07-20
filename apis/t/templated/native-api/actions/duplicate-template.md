# Duplicate Template with Templated

Duplicates an existing template in Templated.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/template/:id/duplicate`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Duplicate Template](https://templated.io/docs/templates/duplicate/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The template id of the template that you want to duplicate. |
| `name` | query | `string` | no | Optional name for the duplicated template. |
