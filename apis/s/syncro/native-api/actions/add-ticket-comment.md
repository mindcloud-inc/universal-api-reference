# Add Ticket Comment with Syncro

Adds a comment to a ticket in Syncro.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/comment`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Add Ticket Comment](https://api-docs.syncromsp.com/#/Ticket/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro ticket ID. |
| `subject` | body | `string` | yes | — |
| `tech` | body | `string` | no | — |
| `body` | body | `string` | yes | — |
| `hidden` | body | `boolean` | no | — |
| `sms_body` | body | `string` | no | — |
| `do_not_email` | body | `boolean` | no | — |
