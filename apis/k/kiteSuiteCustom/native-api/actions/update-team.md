# Update Team with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/team/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Team](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | Team ID |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `members[]` | body | `array` | yes | — |
