# Add Staff Update with HappyFox

Adds a staff update to a ticket in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket/:ticket_number/staff_update/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Add Staff Update](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staff` | body | `number` | yes | HappyFox staff user ID performing the update. |
| `plaintext` | body | `string` | yes | Staff reply in plain text. |
