# Update Contact with Raklet

## Endpoint

- **Method:** `PUT`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Update Contact](https://api.raklet.com/swagger/ui/index#/Contact/Contact_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `firstName` | body | `string` | yes | Contact first name. |
| `lastName` | body | `string` | yes | Contact last name. |
| `language` | body | `string` | yes | Contact language code. |
