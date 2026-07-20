# Update Contact Address with Raklet

## Endpoint

- **Method:** `PUT`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Update Contact Address](https://api.raklet.com/swagger/ui/index#/ContactAddress/ContactAddress_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Raklet contact membership identifier for the address owner. |
| `id` | path | `string` | yes | Raklet address identifier. |
| `details` | body | `string` | yes | Street or line details for the address. |
| `city` | body | `string` | yes | City for the address. |
| `country` | body | `string` | yes | Country code or country value expected by Raklet for the address. |
