# Add Contact Email with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/emails`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Add Contact Email](https://api.raklet.com/swagger/ui/index#/ContactEmail/ContactEmail_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `emailAddress` | body | `string` | yes | Email address to attach to the contact. |
