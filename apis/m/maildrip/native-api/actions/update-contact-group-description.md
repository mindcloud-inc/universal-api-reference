# Update contact group description with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/contacts/groups/{groupId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Update contact group description](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | ID of the contact group to be updated |
| `description` | body | `string` | no | — |
