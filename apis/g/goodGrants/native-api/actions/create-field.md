# Create field with Good Grants

Creates a new field in Good Grants.

## Endpoint

- **Method:** `POST`
- **Path:** `field`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Create field](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `translated.title.en_US` | body | `string` | yes | Field title |
| `tab` | body | `string` | yes | Tab slug |
| `form` | body | `string` | no | Form slug |
| `translated.help_text.en_US` | body | `string` | no | Help text |
| `translated.hint_text.en_US` | body | `string` | no | Hint text |
| `type` | body | `string` | yes | Field type |
