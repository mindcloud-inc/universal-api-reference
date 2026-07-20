# <img src="https://images.mindcloud.co/apps/icons/hunter_1773439476020.png" alt="Hunter logo" width="28" height="28"> Hunter: Universal API

Find emails, verify contacts, enrich companies, and manage leads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hunter/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hunter.io
- **Vendor API docs:** https://hunter.io/api-documentation/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add Sequence Recipient](actions/add-sequence-recipient.md) | POST |  |
| [Cancel Scheduled Sequence Emails](actions/cancel-scheduled-sequence-emails.md) | PUT |  |
| [List Sequence Recipients](actions/list-sequence-recipients.md) | GET |  |
| [List Sequences](actions/list-sequences.md) | GET |  |
| [Start Sequence](actions/start-sequence.md) | PUT |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Discover Companies](actions/discover-companies.md) | GET |  |
| [Enrich Company](actions/enrich-company.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Person](actions/enrich-person.md) | GET |  |
| [Get Combined Enrichment](actions/get-combined-enrichment.md) | GET |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Attribute](actions/create-custom-attribute.md) | POST |  |
| [Delete Custom Attribute](actions/delete-custom-attribute.md) | DELETE |  |
| [Get Custom Attribute](actions/get-custom-attribute.md) | GET |  |
| [List Custom Attributes](actions/list-custom-attributes.md) | GET |  |
| [Update Custom Attribute](actions/update-custom-attribute.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Count Domain Emails](actions/count-domain-emails.md) | GET |  |
| [Find Email](actions/find-email.md) | GET |  |
| [Search Domain Emails](actions/search-domain-emails.md) | GET |  |
| [Verify Email](actions/verify-email.md) | GET |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST |  |
| [Delete Lead](actions/delete-lead.md) | DELETE |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Update Lead](actions/update-lead.md) | PUT |  |
| [Upsert Lead](actions/upsert-lead.md) | PUT |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Leads List](actions/create-leads-list.md) | POST |  |
| [Delete Leads List](actions/delete-leads-list.md) | DELETE |  |
| [Get Leads List](actions/get-leads-list.md) | GET |  |
| [List Leads Lists](actions/list-leads-lists.md) | GET |  |
| [Update Leads List](actions/update-leads-list.md) | PUT |  |

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET |  |

