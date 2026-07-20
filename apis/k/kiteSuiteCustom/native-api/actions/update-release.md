# Update Release with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/release/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Release](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | Release ID |
| `title` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `startDate` | body | `string` | yes | — |
| `releaseDate` | body | `string` | yes | — |
| `manager` | body | `string` | yes | — |
| `status` | body | `string` | yes | — |
| `resources[]` | body | `array` | yes | — |
