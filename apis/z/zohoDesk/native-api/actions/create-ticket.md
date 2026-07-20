# Create Ticket with Zoho Desk

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [Create Ticket](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | Subject of the new ticket. |
| `departmentId` | body | `string` | yes | Department that will own the new ticket. |
| `contactId` | body | `string` | yes | Contact who raised the new ticket. |
| `status` | body | `string` | yes | Status for the new ticket. |
