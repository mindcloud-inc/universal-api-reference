# Update Epic with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/epic/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Epic](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Epic ID |
| `summary` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `assigneeID` | body | `string` | yes | — |
| `reporter` | body | `string` | yes | — |
| `labels[]` | body | `array` | yes | — |
| `listID` | body | `string` | yes | — |
| `parentEpic` | body | `string` | yes | — |
| `linkEpics[]` | body | `array` | yes | — |
| `comments[]` | body | `array` | yes | — |
| `watched[]` | body | `array` | yes | — |
| `attachment[]` | body | `array` | yes | — |
