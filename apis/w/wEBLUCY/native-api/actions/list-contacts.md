# List Contacts with WEBLUCY

Retrieves contacts from WEBLUCY.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [List Contacts](https://websitebuilder.docs.apiary.io/#reference/contacts/list-and-create/list-all-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at_max` | query | `string` | no | List only contacts created before this Unix timestamp, inclusive. |
| `created_at_min` | query | `string` | no | List only contacts created after this Unix timestamp, inclusive. |
