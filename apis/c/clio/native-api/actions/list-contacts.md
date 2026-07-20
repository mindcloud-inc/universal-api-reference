# List Contacts with Clio Manage

Retrieves contacts from your Clio Manage account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [List Contacts](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Wildcard search for contact name, title, email, address, phone number, website, instant messenger address, custom fields, related matter name, or company name. |
| `client_only` | query | `boolean` | no | Filter contacts to only those that are clients. |
| `updated_since` | query | `date` | no | Filter contacts to those updated after a specific ISO-8601 timestamp. |
