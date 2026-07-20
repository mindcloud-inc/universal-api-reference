# <img src="https://images.mindcloud.co/apps/icons/remindlo_1775834415724.png" alt="Remindlo logo" width="28" height="28"> Remindlo: Universal API

SMS reminder platform for managing reminder campaigns, contacts, one-time messages, and webhook endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remindlo/latest
- **Category:** Productivity / Scheduling
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.remindlo.co.uk
- **Vendor API docs:** https://www.remindlo.co.uk/help/sms-reminder-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Campaign Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Enroll Contact In Campaign](actions/enroll-contact-in-campaign.md) | POST |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Upsert Contact](actions/upsert-contact.md) | POST |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

