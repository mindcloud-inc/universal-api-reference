# Set Primary Contact Email with Raklet

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/emails/:id/SetPrimary`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Set Primary Contact Email](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_SetPrimary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `id` | path | `string` | yes | Contact email identifier in Raklet. |
