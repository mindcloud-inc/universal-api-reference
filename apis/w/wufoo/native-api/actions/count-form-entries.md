# Count Form Entries with Wufoo

Retrieves the entry count for a Wufoo form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:identifier/entries/count.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [Count Form Entries](https://wufoo.github.io/docs/#entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The form hash or identifier that owns the entries to count. |
