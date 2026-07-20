# Create Ticket URL with Ticket Generator

Creates a QR code ticket URL in Ticket Generator.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/ticket/url/`
- **Base URL:** `https://apis.ticket-generator.com/client`
- **Official documentation:** [Create Ticket URL](https://apis.ticket-generator.com/client/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | query | `string` | yes | Ticket Generator event identifier. |
| `ticketCategoryId` | query | `string` | no | Ticket category identifier. Optional when the event has exactly one ticket category. |
| `header_1` | body | `string` | no | Variable information field label 1. |
| `value_1` | body | `string` | no | Variable information field value 1. |
| `header_2` | body | `string` | no | Variable information field label 2. |
| `value_2` | body | `string` | no | Variable information field value 2. |
| `header_3` | body | `string` | no | Variable information field label 3. |
| `value_3` | body | `string` | no | Variable information field value 3. |
| `header_4` | body | `string` | no | Variable information field label 4. |
| `value_4` | body | `string` | no | Variable information field value 4. |
| `header_5` | body | `string` | no | Variable information field label 5. |
| `value_5` | body | `string` | no | Variable information field value 5. |
