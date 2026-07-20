# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-31-at-15_1774980163214.png" alt="Pitchbox logo" width="28" height="28"> Pitchbox: Universal API

Pitchbox is a link building, influencer outreach, and content promotion platform with API access to campaigns, projects, opportunities, contacts, emails, and reports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pitchbox/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pitchbox.com
- **Vendor API docs:** https://apiv2.pitchbox.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign By Id](actions/get-campaign-by-id.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

### Campaign Outreach Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Outreach Settings](actions/get-campaign-outreach-settings.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact By Id](actions/get-contact-by-id.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |

### Discovery Type

| Action | Method | Description |
| --- | --- | --- |
| [List Discovery Types](actions/list-discovery-types.md) | GET |  |

### Email Account

| Action | Method | Description |
| --- | --- | --- |
| [List Email Accounts](actions/list-email-accounts.md) | GET |  |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Form Submissions](actions/list-form-submissions.md) | GET |  |

### Inbound Email

| Action | Method | Description |
| --- | --- | --- |
| [List Inbound Emails](actions/list-inbound-emails.md) | GET |  |

### Metrics Filter Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Metrics Filter Template](actions/create-metrics-filter-template.md) | POST |  |
| [Delete Metrics Filter Template](actions/delete-metrics-filter-template.md) | DELETE |  |
| [List Metrics Filter Templates](actions/list-metrics-filter-templates.md) | GET |  |
| [Update Metrics Filter Template](actions/update-metrics-filter-template.md) | PUT |  |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Milestones](actions/list-opportunity-milestones.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity By Id](actions/get-opportunity-by-id.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |

### Opportunity Custom Field Value

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Custom Field Values](actions/list-opportunity-custom-field-values.md) | GET |  |

### Opportunity Milestone History

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Milestone History](actions/list-opportunity-milestone-history.md) | GET |  |

### Opportunity Personalization Field Value

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Personalization Field Values](actions/list-opportunity-personalization-field-values.md) | GET |  |

### Outreach Email

| Action | Method | Description |
| --- | --- | --- |
| [List Outreach Emails](actions/list-outreach-emails.md) | GET |  |

### Personalization Field

| Action | Method | Description |
| --- | --- | --- |
| [List Personalization Fields](actions/list-personalization-fields.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Reports Info](actions/get-reports-info.md) | GET |  |

### Sent Reply Email

| Action | Method | Description |
| --- | --- | --- |
| [List Sent Reply Emails](actions/list-sent-reply-emails.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Campaign Tag](actions/add-campaign-tag.md) | POST |  |
| [Delete Campaign Tag](actions/delete-campaign-tag.md) | DELETE |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |

