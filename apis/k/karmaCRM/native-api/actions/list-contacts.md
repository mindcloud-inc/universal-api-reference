# List Contacts with Karma CRM

Retrieves a list of contacts from Karma CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/contacts.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [List Contacts](https://docs.karmacrm.com/#get-all-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `filters[user_id]` | query | `number` | no | Filter contacts by assigned user ID. |
| `filters[contact_status_id]` | query | `number` | no | Filter contacts by contact status ID. |
| `filters[contact_stage_id]` | query | `number` | no | Filter contacts by contact stage ID. |
| `filters[tag_list]` | query | `string` | no | Comma-separated tag list filter, for example eastern,night. |
