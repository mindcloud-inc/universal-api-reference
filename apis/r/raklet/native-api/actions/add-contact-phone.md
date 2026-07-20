# Add Contact Phone with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/contacts/:organisationMembershipId/phones`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Add Contact Phone](https://api.raklet.com/swagger/ui/index#/ContactPhone/ContactPhone_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | path | `string` | yes | Contact membership identifier in Raklet. |
| `countryCode` | body | `string` | yes | Phone country code. |
| `number` | body | `string` | yes | Phone number. |
