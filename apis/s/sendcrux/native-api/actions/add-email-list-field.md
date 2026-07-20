# Add Email List Field with Sendcrux

Creates a custom field for an email list in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/lists/:uid/add-field`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Add Email List Field](https://api.sendbound.com/email-list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `default_value` | body | `string` | no | The default value for the custom field. |
| `label` | body | `string` | yes | The display label for the new custom field. |
| `tag` | body | `string` | yes | The unique field tag used by Sendcrux for this custom field. |
| `type` | body | `string` | yes | The Sendcrux field type, such as text. |
| `uid` | path | `string` | yes | The unique identifier of the list to extend with a custom field. |
