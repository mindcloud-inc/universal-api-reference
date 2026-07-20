# Create Letter with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/letters`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Create Letter](https://docs.lob.com/#tag/Letters/operation/letter_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the letter job. |
| `to` | body | `string` | yes | Recipient address ID. |
| `from` | body | `string` | yes | Sender address ID. |
| `file` | body | `string` | yes | Letter artwork file, template ID, HTML, or remote file URL. |
| `color` | body | `boolean` | yes | Whether to print the letter in color. |
| `use_type` | body | `string` | yes | Declared mail use type. |
