# List Contact Email Addresses with Clio Manage

Retrieves email addresses for a contact in Clio Manage.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id/email_addresses.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [List Contact Email Addresses](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Email%20Addresses/operation/EmailAddress%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The Clio contact ID. |
