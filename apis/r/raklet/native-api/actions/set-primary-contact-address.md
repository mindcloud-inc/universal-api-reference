# Set Primary Contact Address with Raklet

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id/SetPrimary`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Set Primary Contact Address](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_SetPrimary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Raklet contact membership identifier for the address owner. |
| `id` | path | `string` | yes | Raklet address identifier to promote as primary. |
