# Close Session with LogMeIn

Closes an existing support session in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve/v1/sessions/:sessionId/close`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Close Session](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Required session ID to close. |
