# List Open Invitations For Invitee with Vortex

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/invitations`
- **Base URL:** `https://api.vortexsoftware.com`
- **Official documentation:** [List Open Invitations For Invitee](https://docs.vortexsoftware.com/api-reference/invitations/get-open-invitations-for-an-invitee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetType` | query | `string` | yes | Invitee target type. |
| `targetValue` | query | `string` | yes | Invitee target value, such as an email address or phone number. |
