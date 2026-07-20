# <img src="https://images.mindcloud.co/apps/icons/62449537809bb9263d1cdacc-logo2_1773255316218.png" alt="RD Station Marketing logo" width="28" height="28"> RD Station Marketing: Universal API

RD Station Marketing: Manage contacts, conversions, events, and marketing workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rDStationMarketing/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rdstation.com/
- **Vendor API docs:** https://developers.rdstation.com/reference/introducao-rdsm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Custom Fields](actions/list-custom-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversion Asset Statistics](actions/get-conversion-asset-statistics.md) | GET |  |
| [Get Email Marketing Statistics](actions/get-email-marketing-statistics.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag to Contact by UUID or Email](actions/add-tag-to-contact-by-uuid-or-email.md) | POST |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact by UUID or Email](actions/delete-contact-by-uuid-or-email.md) | DELETE |  |
| [Get Contact by UUID or Email](actions/get-contact-by-uuid-or-email.md) | GET |  |
| [Get Contact Default Funnel by UUID or Email](actions/get-contact-default-funnel-by-uuid-or-email.md) | GET |  |
| [List Contact Events](actions/list-contact-events.md) | GET |  |
| [Update Contact by UUID or Email](actions/update-contact-by-uuid-or-email.md) | PUT |  |
| [Update Contact Default Funnel by UUID or Email](actions/update-contact-default-funnel-by-uuid-or-email.md) | PUT |  |

### Contact Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE |  |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |
| [Update Custom Field](actions/update-custom-field.md) | PUT |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email by ID](actions/get-email-by-id.md) | GET |  |
| [List Emails](actions/list-emails.md) | GET |  |

### Embeddable

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET |  |

### Landing Page

| Action | Method | Description |
| --- | --- | --- |
| [List Landing Pages](actions/list-landing-pages.md) | GET |  |

### Popup

| Action | Method | Description |
| --- | --- | --- |
| [List Popups](actions/list-popups.md) | GET |  |

### Segmentation

| Action | Method | Description |
| --- | --- | --- |
| [List Segmentation Contacts](actions/list-segmentation-contacts.md) | GET |  |
| [List Segmentations](actions/list-segmentations.md) | GET |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Add Leads to Workflow](actions/add-leads-to-workflow.md) | POST |  |
| [Get Workflow by ID](actions/get-workflow-by-id.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |

