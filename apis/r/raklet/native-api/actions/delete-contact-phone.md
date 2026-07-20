# Delete Contact Phone with Raklet

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/phones/:id`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Delete Contact Phone](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_Delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `id` | path | `string` | yes | Contact phone identifier in Raklet. |
