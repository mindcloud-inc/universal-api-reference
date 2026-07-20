# Delete Contact Note with Umbler Talk

Deletes a contact note from Umbler Talk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/contacts/[:id]/notes/[:noteId]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Delete Contact Note](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The contact ID. |
| `noteId` | path | `string` | yes | The note ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
