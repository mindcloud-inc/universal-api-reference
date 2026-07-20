# Submit Form Entry with Wufoo

Creates a new entry in a specific Wufoo form.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:identifier/entries.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [Submit Form Entry](https://wufoo.github.io/docs/#entries)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The form hash or identifier that will receive the submitted entry. |
