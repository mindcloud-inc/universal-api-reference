# Add Communication Record with Cloze

Creates a communication record in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/timeline/communication/create`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Add Communication Record](https://api.cloze.com/api-docs/#/paths/v1-timeline-communication-create/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | no | When the communication happened. |
| `bodytype` | body | `string` | no | Type of the body. |
| `style` | body | `string` | no | Style of the communication. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `from` | body | `string` | no | Address of the person initiating the communication. |
| `recipients[]` | body | `array<object>` | no | Recipients or attendees for the communication. |
| `recipients[].value` | body | `string` | no | Identifier for the recipient. |
| `subject` | body | `string` | no | Subject of the communication. |
| `body` | body | `string` | no | Body text of the communication. |
