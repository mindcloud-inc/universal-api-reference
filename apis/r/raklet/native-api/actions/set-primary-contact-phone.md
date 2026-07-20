# Set Primary Contact Phone with Raklet

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/phones/:id/SetPrimary`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Set Primary Contact Phone](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_SetPrimary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `id` | path | `string` | yes | Contact phone identifier in Raklet. |
