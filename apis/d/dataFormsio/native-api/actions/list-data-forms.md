# List Data Forms with DataForms.io

Retrieves data forms from DataForms.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/dataforms`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [List Data Forms](https://dataforms.readme.io/reference/index-data-forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Filter data forms by search term. |
| `limit` | query | `number` | no | Limit the number of forms returned. Maximum 50. |
