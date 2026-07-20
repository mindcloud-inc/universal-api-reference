# Mark Work Ticket As Reviewed with Aspire

Marks a work ticket as reviewed in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `WorkTicketStatus/MarkWorkTicketAsReviewed`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Mark Work Ticket As Reviewed](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketStatus/WorkTicketStatus_MarkWorkTicketAsReviewed)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `WorkTicketID` | body | `number` | yes |
| `ReviewedDateTime` | body | `date` | yes |
| `ReviewedUserID` | body | `number` | no |
