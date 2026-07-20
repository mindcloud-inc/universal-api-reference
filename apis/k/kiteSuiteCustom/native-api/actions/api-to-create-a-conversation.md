# Api to create a conversation with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Api to create a conversation](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `name` | body | `string` | yes | — |
| `members[]` | body | `array` | yes | — |
| `type` | body | `string` | yes | — |
| `projectID` | body | `string` | yes | — |
| `message` | body | `string` | yes | — |
