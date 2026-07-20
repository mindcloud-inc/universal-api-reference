# List Contact Notes with Umbler Talk

Retrieves a contact's notes from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/[:id]/notes/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Contact Notes](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The contact ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
