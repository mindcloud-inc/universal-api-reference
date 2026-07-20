# Create Link with Freshworks CRM

Creates a document link in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/document_links`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Link](https://developers.freshworks.com/crm/api/#create_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Link URL |
| `name` | body | `string` | no | Optional display name for the link |
| `is_shared` | body | `boolean` | no | Share the created link |
| `targetable_id` | body | `number` | yes | ID of the contact, sales account, or deal |
| `targetable_type` | body | `string` | yes | Entity type: Contact, SalesAccount, or Deal |
