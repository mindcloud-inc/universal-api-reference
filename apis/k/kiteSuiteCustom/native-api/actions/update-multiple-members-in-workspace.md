# Update multiple members in workspace. with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspace/member/multiple`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update multiple members in workspace.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `members[]` | body | `array` | yes | — |
| `role` | body | `string` | yes | — |
| `action` | body | `string` | yes | — |
