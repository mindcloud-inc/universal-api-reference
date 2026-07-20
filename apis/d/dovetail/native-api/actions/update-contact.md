# Update Contact with Dovetail

Updates an existing contact in Dovetail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contacts/:contactId`
- **Base URL:** `https://dovetail.com/api`
- **Official documentation:** [Update Contact](https://developers.dovetail.com/reference/patch_v1-contacts-contactid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | — |
| `email` | body | `string` | no | Contact email. |
| `name` | body | `string` | no | Contact name. |
