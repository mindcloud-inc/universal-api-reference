# List Contacts with BigMailer

Retrieves contacts from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/contacts`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [List Contacts](https://docs.bigmailer.io/reference/listcontacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to list contacts in. |
| `list_id` | query | `string` | no | Filter contacts to a specific list. |
