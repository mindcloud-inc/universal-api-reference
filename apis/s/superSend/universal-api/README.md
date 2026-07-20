# <img src="https://images.mindcloud.co/apps/icons/super-send_1775142399349.png" alt="SuperSend logo" width="28" height="28"> SuperSend: Universal API

Manage contacts, campaigns, conversations, and deliverability in SuperSend

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/superSend/latest
- **Category:** Marketing
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.supersend.io
- **Vendor API docs:** https://docs.supersend.io/docs/v2-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [List Announcements](actions/list-announcements.md) | GET | Retrieves announcements from SuperSend. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in SuperSend. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from SuperSend. |
| [Get Campaign Sequence](actions/get-campaign-sequence.md) | GET | Retrieves a campaign sequence from SuperSend. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from SuperSend. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in SuperSend. |
| [Update Campaign Sequence](actions/update-campaign-sequence.md) | PUT | Updates a campaign sequence in SuperSend. |

### Capacity Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Capacity Summary](actions/get-capacity-summary.md) | GET | Retrieves the capacity summary from SuperSend. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign Category](actions/create-campaign-category.md) | POST | Creates a new campaign category in SuperSend. |
| [Delete Campaign Category](actions/delete-campaign-category.md) | DELETE | Deletes an existing campaign category from SuperSend. |
| [List Campaign Categories](actions/list-campaign-categories.md) | GET | Retrieves campaign categories from SuperSend. |
| [Update Campaign Category](actions/update-campaign-category.md) | PUT | Updates an existing campaign category in SuperSend. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Assign Label to Contact Profile](actions/assign-label-to-contact-profile.md) | POST | Assigns a profile label to a SuperSend contact. |
| [Bulk Import Contacts](actions/bulk-import-contacts.md) | POST | Creates multiple contacts in SuperSend. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in SuperSend. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from SuperSend. |
| [Delete Contact by Identifier](actions/delete-contact-by-identifier.md) | DELETE | Deletes contacts from SuperSend by identifier. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from SuperSend. |
| [List Contact Profile Labels](actions/list-contact-profile-labels.md) | GET | Retrieves profile labels for a SuperSend contact. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from SuperSend. |
| [Remove Contact Profile Label](actions/remove-contact-profile-label.md) | DELETE | Deletes a profile label from a SuperSend contact. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in SuperSend. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from SuperSend. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from SuperSend. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in SuperSend. |

### Deliverability Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Deliverability Summary](actions/get-deliverability-summary.md) | GET | Retrieves the deliverability summary from SuperSend. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from SuperSend. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from SuperSend. |
| [Purchase Domains](actions/purchase-domains.md) | POST | Creates managed domains in SuperSend. |
| [Purchase Domains and Mailboxes](actions/purchase-domains-and-mailboxes.md) | POST | Creates managed domains and mailboxes in SuperSend. |

### Domain Health Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Health Summary](actions/get-domain-health-summary.md) | GET | Retrieves the domain health summary from SuperSend. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email (SMTP)](actions/verify-email-smtp.md) | POST | Verifies an email in SuperSend using SMTP. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from SuperSend. |
| [List Events](actions/list-events.md) | GET | Retrieves events from SuperSend. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Get Health Check](actions/get-health-check.md) | GET | Retrieves the SuperSend service health status. |

### Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [Purchase Mailboxes](actions/purchase-mailboxes.md) | POST | Creates managed mailboxes in SuperSend. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Messages](actions/get-conversation-messages.md) | GET | Retrieves messages from a SuperSend conversation. |
| [Send Conversation Message](actions/send-conversation-message.md) | POST | Creates a message in a SuperSend conversation. |

### Outbound Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Outbound Summary](actions/get-outbound-summary.md) | GET | Retrieves the outbound summary from SuperSend. |

### Placement Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Placement Test](actions/create-placement-test.md) | POST | Creates a new placement test in SuperSend. |
| [Export Placement Tests](actions/export-placement-tests.md) | POST | Creates a placement test export in SuperSend. |
| [Get Placement Test](actions/get-placement-test.md) | GET | Retrieves a placement test from SuperSend. |
| [List Placement Tests](actions/list-placement-tests.md) | GET | Retrieves placement tests from SuperSend. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Get Sender](actions/get-sender.md) | GET | Retrieves a sender from SuperSend. |
| [List Senders](actions/list-senders.md) | GET | Retrieves senders from SuperSend. |
| [Update Sender](actions/update-sender.md) | PUT | Updates an existing sender in SuperSend. |

### Sender Health Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Sender Health Summary](actions/get-sender-health-summary.md) | GET | Retrieves the sender health summary from SuperSend. |

### Team Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Cost Allocation](actions/get-team-cost-allocation.md) | GET | Retrieves team cost allocation from SuperSend. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST | Creates a new team in SuperSend. |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from SuperSend. |
| [Get Team Usage](actions/get-team-usage.md) | GET | Retrieves team usage from SuperSend. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from SuperSend. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in SuperSend. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from SuperSend. |

### Webhook Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Delivery](actions/get-webhook-delivery.md) | GET | Retrieves a webhook delivery from SuperSend. |
| [List Webhook Deliveries](actions/list-webhook-deliveries.md) | GET | Retrieves webhook deliveries from SuperSend. |
| [Retry Webhook Delivery](actions/retry-webhook-delivery.md) | POST | Retries a webhook delivery in SuperSend. |

