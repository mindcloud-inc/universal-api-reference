# Invite Company To Portal with SWELLEnterprise

Sends a portal invitation to a company in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/client-portal/companies/:companyId/invite`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Invite Company To Portal](https://dashboard.swellsystem.com/docs#client-portal-POSTapi-v1-client-portal-companies--companyId--invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | The ID of the company to invite. |
| `custom_message` | body | `string` | no | Optional custom message to include in the invitation email. |
