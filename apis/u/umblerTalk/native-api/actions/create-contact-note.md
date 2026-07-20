# Create Contact Note with Umbler Talk

Creates a contact note in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/[:id]/notes/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Create Contact Note](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Note content. |
| `id` | path | `string` | yes | The contact ID. |
| `organizationId` | body | `string` | yes | The organization ID. |
