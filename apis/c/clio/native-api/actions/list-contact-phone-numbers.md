# List Contact Phone Numbers with Clio Manage

Retrieves phone numbers for a contact in Clio Manage.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id/phone_numbers.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [List Contact Phone Numbers](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Phone%20Numbers/operation/PhoneNumber%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The Clio contact ID. |
