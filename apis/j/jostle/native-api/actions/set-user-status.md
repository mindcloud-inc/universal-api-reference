# Set User Status with Jostle

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/people/status`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [Set User Status](https://api.jostle.me/reference/setuserstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user.userId` | body | `string` | yes | Id of the user |
| `type` | body | `string` | yes | The type of user status |
| `resetAfter` | body | `string` | yes | When the user status should clear itself |
| `statusMessage` | body | `string` | no | User-specified status message when type is CUSTOM |
| `emoji` | body | `string` | no | User-specified emoji when type is CUSTOM |
