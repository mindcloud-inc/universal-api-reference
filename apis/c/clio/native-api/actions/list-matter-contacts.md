# List Matter Contacts with Clio Manage

Retrieves contacts for a matter in Clio Manage.

## Endpoint

- **Method:** `GET`
- **Path:** `/matters/:matter_id/contacts.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [List Matter Contacts](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Matter%20Contacts/operation/MatterContacts%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matter_id` | path | `number` | yes | The Clio matter ID. |
