# Fill Form With Automation with Airtop

Fills a form synchronously with an Airtop automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/fill-form`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Fill Form With Automation](https://docs.airtop.ai/api-reference/airtop-api/windows/fill-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `automationId` | body | `string` | yes |
