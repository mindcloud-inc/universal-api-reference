# Add members in workspace. with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspace/member`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add members in workspace.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `members[]` | body | `array` | yes | — |
| `role` | body | `string` | yes | — |
