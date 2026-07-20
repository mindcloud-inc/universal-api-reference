# List Project Access Users with Documenterra

Retrieves users with project access from Documenterra.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/users`
- **Base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`
- **Official documentation:** [List Project Access Users](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-poluchenie-spiska-polzovateley-s-dostupom-k-proektu-publikatsii)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Documenterra project or publication identifier. |
| `types` | query | `string` | no | Optional comma-separated user access types filter. |
