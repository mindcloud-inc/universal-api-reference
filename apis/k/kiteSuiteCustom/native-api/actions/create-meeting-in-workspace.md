# Create meeting in workspace. with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/meeting`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create meeting in workspace.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `startDate` | body | `string` | yes | — |
| `endDate` | body | `string` | yes | — |
| `members[]` | body | `array` | yes | — |
