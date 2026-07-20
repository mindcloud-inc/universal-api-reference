# Count Report Entries with Wufoo

Retrieves the entry count for a Wufoo report.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:identifier/entries/count.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [Count Report Entries](https://wufoo.github.io/docs/#reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The report hash or identifier whose entries to count. |
