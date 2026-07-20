# Get Session Mailto Link with LogMeIn

Retrieves a session email invitation link from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/goto-resolve/v1/sessions/:sessionId/invite/email`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Get Session Mailto Link](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Required session ID to generate the mailto invite link for. |
| `language` | query | `string` | yes | Required language code for the mailto link. |
