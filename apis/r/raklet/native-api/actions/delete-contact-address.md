# Delete Contact Address with Raklet

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Delete Contact Address](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_Delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Raklet contact membership identifier for the address owner. |
| `id` | path | `string` | yes | Raklet address identifier to delete. |
