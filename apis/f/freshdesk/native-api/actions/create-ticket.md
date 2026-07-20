# Create Ticket with Freshdesk

Creates a new ticket in Freshdesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Create Ticket](https://developers.freshdesk.com/api/#create_ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the requester |
| `requester_id` | body | `list<number>` | no | User ID of the requester |
| `email` | body | `string` | no | Email address of the requester |
| `facebook_id` | body | `string` | no | Facebook ID of the requester |
| `phone` | body | `string` | no | Phone number of the requester |
| `twitter_id` | body | `string` | no | Twitter handle of the requester |
| `unique_external_id` | body | `string` | no | External ID of the requester |
| `subject` | body | `string` | no | Subject of the ticket |
| `type` | body | `string` | no | Ticket type/category |
| `status` | body | `number` | no | Status of the ticket |
| `priority` | body | `number` | no | Priority of the ticket |
| `description` | body | `string` | no | HTML content of the ticket |
| `responder_id` | body | `list<number>` | no | ID of the assigned agent |
| `attachments[]` | body | `array<object>` | no | Ticket attachments |
| `cc_emails[]` | body | `array<string>` | no | Email addresses added in CC |
| `custom_fields` | body | `object` | no | Key-value pairs for custom ticket fields |
| `due_by` | body | `date` | no | SLA due date/time for the ticket |
| `email_config_id` | body | `number` | no | Email configuration ID for the ticket |
| `fr_due_by` | body | `date` | no | First response due date/time |
| `group_id` | body | `number` | no | Group ID assigned to the ticket |
| `parent_id` | body | `list<number>` | no | Parent ticket ID for child-ticket linking |
| `product_id` | body | `number` | no | Product ID associated with the ticket |
| `source` | body | `number` | no | Source channel through which the ticket was created |
| `tags[]` | body | `array<string>` | no | Tags associated with the ticket |
| `company_id` | body | `list<number>` | no | Company ID of the requester |
| `internal_agent_id` | body | `list<number>` | no | Internal agent ID to assign |
| `internal_group_id` | body | `number` | no | Internal group ID to assign |
| `lookup_parameter` | body | `string` | no | Lookup field value for custom object linkage |
