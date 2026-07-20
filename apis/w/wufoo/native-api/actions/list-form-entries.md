# List Form Entries with Wufoo

Retrieves entries from a specific Wufoo form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:identifier/entries.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [List Form Entries](https://wufoo.github.io/docs/#entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The Wufoo form hash or URL slug, for example `z18tlglo01kf7h1`. |
