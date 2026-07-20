# List Outlines with Toodledo

Retrieves outlines from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/outlines/get.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Outlines](https://api.toodledo.com/3/outlines/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `number` | no | Return only outlines modified before this GMT Unix timestamp. |
| `after` | query | `number` | no | Return only outlines modified after this GMT Unix timestamp. |
| `id` | query | `string` | no | Fetch a single outline by its hexadecimal Toodledo outline ID. |
| `start` | query | `number` | no | Number of records to skip before returning results. |
| `num` | query | `number` | no | Maximum number of outlines to return. Toodledo documents a default and max of 1000. |
