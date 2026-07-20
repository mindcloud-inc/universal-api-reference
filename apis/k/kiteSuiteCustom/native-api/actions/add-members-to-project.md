# Add Members to project. with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/project/member`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Add Members to project.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `projectID` | body | `string` | yes | — |
| `members[]` | body | `array` | yes | — |
| `roleID` | body | `string` | yes | — |
