# Generate Memory Grid with Shadify

Retrieves a random memory grid from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/memory/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Memory Grid](https://shadify.yurace.pro/modules/memory.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | query | `number` | no | Optional grid width. Default is 6. |
| `height` | query | `number` | no | Optional grid height. Default is 4. |
| `pair-size` | query | `number` | no | Optional matching group size. Available values are 2, 3, and 4. Default is 3. |
| `show-positions` | query | `boolean` | no | Optional true or false value that includes positions for each pair. Default is true. |
