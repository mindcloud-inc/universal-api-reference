# Generate Schulte Table with Shadify

Retrieves a random Schulte table from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/schulte/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Schulte Table](https://shadify.yurace.pro/modules/schulte.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `size` | query | `number` | no | Optional table size from 1 to 15. Default is 5. |
| `mode` | query | `list` | no | Optional number or alphabet mode. Default is number. Accepted values: `0`, `1`. |
