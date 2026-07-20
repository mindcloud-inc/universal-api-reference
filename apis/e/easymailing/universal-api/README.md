# <img src="https://images.mindcloud.co/apps/icons/easymailing_1775079785834.png" alt="Easymailing logo" width="28" height="28"> Easymailing: Universal API

Easymailing is an email marketing platform for managing audiences, subscribers, campaigns, templates, automations, and account configuration through a REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easymailing/latest
- **Category:** Communication / Email Communications
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://easymailing.com/
- **Vendor API docs:** https://developers.easymailing.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Subscription](actions/get-my-subscription.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-my-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Member Activities](actions/list-member-activities.md) | GET | Retrieves member activities from Easymailing. |

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [Get Audience](actions/get-audience.md) | GET | Retrieves an audience from Easymailing. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from Easymailing. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Easymailing. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Easymailing. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Audience Member](actions/get-audience-member.md) | GET | Retrieves an audience member from Easymailing. |
| [List Audience Members](actions/list-audience-members.md) | GET | Retrieves audience members from Easymailing. |
| [Search Members](actions/search-members.md) | GET | Finds members in Easymailing by search query. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Condition Field](actions/get-condition-field.md) | GET | Retrieves a condition field from Easymailing. |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from Easymailing. |
| [List Condition Fields](actions/list-condition-fields.md) | GET | Retrieves condition fields from Easymailing. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Easymailing. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Form](actions/get-subscription-form.md) | GET | Retrieves a subscription form from Easymailing. |
| [Get Subscription Form Publishing Info](actions/get-subscription-form-publishing-info.md) | GET | Retrieves subscription form publishing info from Easymailing. |
| [List Subscription Forms](actions/list-subscription-forms.md) | GET | Retrieves subscription forms from Easymailing. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Easymailing. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Easymailing. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Easymailing. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Easymailing. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [List Support Tickets](actions/list-support-tickets.md) | GET | Retrieves support tickets from Easymailing. |

### Journeys

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation](actions/get-automation.md) | GET | Retrieves an automation from Easymailing. |
| [List Automations](actions/list-automations.md) | GET | Retrieves automations from Easymailing. |

### Queues

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation Queue](actions/get-automation-queue.md) | GET | Retrieves an automation queue from Easymailing. |
| [List Automation Queues](actions/list-automation-queues.md) | GET | Retrieves automation queues from Easymailing. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Easymailing. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Easymailing. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get My Subscription](actions/get-my-subscription.md) | GET | Retrieves your subscription from Easymailing. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Easymailing. |
| [Get Template Schema](actions/get-template-schema.md) | GET | Retrieves the template schema from Easymailing. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Easymailing. |

