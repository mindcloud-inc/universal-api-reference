# Bulk Add Contacts to Blacklist with JustCall

Adds contacts to the JustCall blacklist.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2.1/contacts/bulk-add/blacklist`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Bulk Add Contacts to Blacklist](https://developer.justcall.io/reference/bulk_add_contacts_to_blacklist_v21)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `add_to[]` | body | `array<string>` | yes | Status lists to add these contacts to. |
| `contact_numbers[]` | body | `array<string>` | yes | Contact numbers to blacklist. |
