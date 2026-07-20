# Get Session State with LogMeIn

Retrieves a support session state from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/goto-resolve/v1/sessions/:sessionId`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Get Session State](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Required session ID to retrieve. |
