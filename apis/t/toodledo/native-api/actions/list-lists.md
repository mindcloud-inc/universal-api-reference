# List Lists with Toodledo

Retrieves lists from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/get.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Lists](https://api.toodledo.com/3/lists/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `number` | no | Return only lists modified before this GMT Unix timestamp. |
| `after` | query | `number` | no | Return only lists modified after this GMT Unix timestamp. |
| `id` | query | `string` | no | Fetch a single list by its hexadecimal Toodledo list ID. |
| `start` | query | `number` | no | Number of records to skip before returning results. |
| `num` | query | `number` | no | Maximum number of lists to return. Toodledo documents a default and max of 1000. |
