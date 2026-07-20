# Update Contact Email with Raklet

## Endpoint

- **Method:** `PUT`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/emails/:id`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Update Contact Email](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `id` | path | `string` | yes | Contact email identifier in Raklet. |
| `emailAddress` | body | `string` | yes | Email address value. |
