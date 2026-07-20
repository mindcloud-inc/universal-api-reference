# Get Parent Ticket with Jitbit Helpdesk

## Endpoint

- **Method:** `GET`
- **Path:** `/ParentTicket`
- **Base URL:** `{helpdeskBaseUrl}/api`
- **Official documentation:** [Get Parent Ticket](https://www.jitbit.com/docs/api/#parent-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | Jitbit child ticket ID. |
| `returnFullTicket` | query | `boolean` | no | Set true to return the full parent ticket object instead of only the parent ticket ID. |
