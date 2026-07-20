# List Form Fields with Wufoo

Retrieves fields from a specific Wufoo form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:identifier/fields.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [List Form Fields](https://wufoo.github.io/docs/#forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The Wufoo form hash or URL slug, for example `z18tlglo01kf7h1`. |
