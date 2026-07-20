# Download Invoice with pretix

Retrieves an invoice download from pretix.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizer/events/:event/invoices/:invoice/download/`
- **Base URL:** `https://pretix.eu/api/v1`
- **Official documentation:** [Download Invoice](https://docs.pretix.eu/dev/api/resources/invoices.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer` | path | `string` | yes | pretix organizer slug. |
| `event` | path | `string` | yes | pretix event slug. |
| `invoice` | path | `string` | yes | pretix invoice number. |
