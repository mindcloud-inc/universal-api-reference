# Update Contact Phone with Raklet

## Endpoint

- **Method:** `PUT`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/phones/:id`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Update Contact Phone](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `id` | path | `string` | yes | Contact phone identifier in Raklet. |
| `countryCode` | body | `string` | yes | Phone country code. |
| `number` | body | `string` | yes | Phone number. |
