# List Report Entries with Wufoo

Retrieves entries from a specific Wufoo report.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:identifier/entries.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [List Report Entries](https://wufoo.github.io/docs/#reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The report hash or identifier whose entries to list. |
