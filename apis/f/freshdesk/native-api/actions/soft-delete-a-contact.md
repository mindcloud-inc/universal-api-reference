# Soft Delete a Contact with Freshdesk

Deletes a contact from Freshdesk without permanently removing it.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/:id`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Soft Delete a Contact](https://developers.freshdesk.com/api/#delete_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<number>` | yes | Freshdesk contact ID. |
