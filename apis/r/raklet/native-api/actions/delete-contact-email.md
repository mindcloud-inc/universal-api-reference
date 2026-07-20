# Delete Contact Email with Raklet

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/emails/:id`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Delete Contact Email](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_Delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `id` | path | `string` | yes | Contact email identifier in Raklet. |
