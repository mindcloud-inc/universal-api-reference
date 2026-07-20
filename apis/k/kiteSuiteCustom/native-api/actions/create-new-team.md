# Create new Team with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/team`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create new Team](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `members[]` | body | `array` | yes | — |
