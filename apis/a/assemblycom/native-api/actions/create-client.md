# Create Client with Assembly.com

Creates a client in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Create Client](https://docs.assembly.com/reference/create-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sendInvite` | query | `boolean` | no | If true then send an account invite to the client. |
| `givenName` | body | `string` | yes | — |
| `familyName` | body | `string` | yes | — |
| `email` | body | `string` | yes | — |
| `companyId` | body | `string` | no | The ID of the company this client belongs to. |
| `customFields` | body | `object` | no | Optional custom field map keyed by Assembly custom field keys. |
