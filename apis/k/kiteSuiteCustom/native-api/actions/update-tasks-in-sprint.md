# Update Tasks in sprint with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sprint/task`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Tasks in sprint](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `newSprint` | body | `string` | yes | — |
| `tasks[]` | body | `array` | yes | — |
| `position` | body | `number` | yes | — |
