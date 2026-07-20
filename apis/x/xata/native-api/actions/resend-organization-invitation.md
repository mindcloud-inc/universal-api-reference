# Resend an invitation with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/invitations/:invitationID/resend`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Resend an invitation](https://xata.io/docs/api-reference/organizations/resend-an-invitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier for a specific organization |
| `invitationID` | path | `string` | yes | Unique identifier for an invitation |
