# Update Client with Assembly.com

Updates an existing client in Assembly.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/clients/:id`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Update Client](https://docs.assembly.com/reference/update-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the client to update |
| `sendInvite` | query | `boolean` | no | Sends an email invitation to the updated client. |
| `givenName` | body | `string` | no | The client's given name. |
| `familyName` | body | `string` | no | The client's family name. |
| `companyId` | body | `string` | no | The ID of the company to assign this client to. |
| `customFields` | body | `object` | no | Optional custom field updates keyed by Assembly custom field keys. |
