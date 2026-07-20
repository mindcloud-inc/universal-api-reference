# Save Profile On Termination with Airtop

Saves a named profile when an Airtop session terminates.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sessions/:sessionId/save-profile-on-termination/:profileName`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Save Profile On Termination](https://docs.airtop.ai/api-reference/airtop-api/sessions/save-profile-on-termination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | — |
| `profileName` | path | `string` | yes | Name under which to save the profile |
