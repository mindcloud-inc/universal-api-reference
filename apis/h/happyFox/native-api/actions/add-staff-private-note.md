# Add Staff Private Note with HappyFox

Adds a private note to a ticket in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/ticket/:ticket_number/staff_pvtnote/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Add Staff Private Note](https://support.happyfox.com/kb/article/1039-tickets-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_number` | path | `string` | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staff` | body | `number` | yes | HappyFox staff user ID authoring the private note. |
| `plaintext` | body | `string` | yes | Private note text in plain text. |
