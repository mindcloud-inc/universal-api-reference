# <img src="https://images.mindcloud.co/apps/icons/id-d35ig-ke-logos_1772746187515.png" alt="MailerLite logo" width="28" height="28"> MailerLite: Universal API

Manage subscribers, send campaigns, automate emails, and grow audiences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailerLite/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailerlite.com
- **Vendor API docs:** https://developers.mailerlite.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Subscribers](actions/list-subscribers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Automation](actions/create-draft-automation.md) | POST | Creates a draft automation in MailerLite. |
| [Get Automation](actions/get-automation.md) | GET | Retrieves a single automation from MailerLite. |
| [List Automations](actions/list-automations.md) | GET | Retrieves a page of automations from MailerLite. |

### Automation Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation Subscriber Activity](actions/get-automation-subscriber-activity.md) | GET | Retrieves subscriber activity for an automation in MailerLite. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Ready Campaign](actions/cancel-ready-campaign.md) | PUT | Cancels a ready campaign in MailerLite. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in MailerLite. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a single campaign from MailerLite. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from MailerLite by status or type. |
| [Schedule Campaign](actions/schedule-campaign.md) | PUT | Schedules a campaign in MailerLite, or sends it immediately. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates a draft campaign in MailerLite. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a subscriber field in MailerLite. |
| [List Fields](actions/list-fields.md) | GET | Retrieves all subscriber fields from MailerLite. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Assign Subscriber to Group](actions/assign-subscriber-to-group.md) | PUT | Assigns an existing subscriber to a group in MailerLite. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in MailerLite. |
| [Import Bulk Subscribers to Group](actions/import-bulk-subscribers-to-group.md) | PUT | Imports multiple subscribers into a group in MailerLite. |
| [List Group Subscribers](actions/list-group-subscribers.md) | GET | Retrieves subscribers from a specific group in MailerLite. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a page of groups from MailerLite. |
| [Unassign Subscriber from Group](actions/unassign-subscriber-from-group.md) | DELETE | Removes a subscriber from a group in MailerLite. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in MailerLite. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves a page of segments from MailerLite. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create or Upsert Subscriber](actions/create-or-upsert-subscriber.md) | POST | Creates a subscriber in MailerLite, or updates one with the same email. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes a subscriber from MailerLite while keeping their information. |
| [Forget Subscriber](actions/forget-subscriber.md) | DELETE | Deletes a subscriber from MailerLite and permanently removes their data. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from MailerLite by ID or email. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves a page of subscribers from MailerLite. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in MailerLite. |

### Subscriber Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber Activity](actions/get-subscriber-activity.md) | GET | Retrieves activity for a subscriber in MailerLite. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in MailerLite. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhook endpoints from MailerLite. |

