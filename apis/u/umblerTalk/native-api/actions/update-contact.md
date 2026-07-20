# Update Contact with Umbler Talk

Updates an existing contact in Umbler Talk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contacts/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Update Contact](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Contact email address. |
| `id` | path | `string` | yes | The contact ID. |
| `name` | body | `string` | no | Contact name. |
| `organizationId` | query | `string` | yes | The organization ID. |
