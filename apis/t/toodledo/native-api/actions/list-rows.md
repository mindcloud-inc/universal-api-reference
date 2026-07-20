# List Rows with Toodledo

Retrieves rows from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/rows/get.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Rows](https://api.toodledo.com/3/rows/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | query | `string` | yes | Hexadecimal list ID whose rows should be fetched. |
| `before` | query | `number` | no | Return only rows modified before this GMT Unix timestamp. |
| `after` | query | `number` | no | Return only rows modified after this GMT Unix timestamp. |
| `id` | query | `string` | no | Fetch a single row by its hexadecimal Toodledo row ID. |
| `start` | query | `number` | no | Number of records to skip before returning results. |
| `num` | query | `number` | no | Maximum number of rows to return. Toodledo documents a default and max of 1000. |
