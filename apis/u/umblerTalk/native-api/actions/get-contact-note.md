# Get Contact Note with Umbler Talk

Retrieves a contact note from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/[:id]/note/[:noteId]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Contact Note](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The contact ID. |
| `noteId` | path | `string` | yes | The note ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
