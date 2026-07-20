# View Person with 4HSE

Retrieves a person from 4HSE.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/person/view/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [View Person](https://docs.4hse.com/en/api/person/#operation-viewPerson-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Person ID. |
| `code` | query | `string` | no | Employee code. Maximum length: 50. |
| `project_id` | query | `string` | no | Project ID when looking up by code. |
