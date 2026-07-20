# <img src="https://images.mindcloud.co/apps/icons/561ab462aa85d05668e24808-favicon_1777052244536.png" alt="PrimeGate logo" width="28" height="28"> PrimeGate: Universal API

PrimeGate: Track leads, manage sales, and analyze marketing performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/primeGate/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.primegate.io
- **Vendor API docs:** https://www.primegate.io/support/rabota-s-api-primegate

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Leads](actions/list-leads.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/primeGate/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact by City](actions/get-contact-by-city.md) | GET |  |
| [Get Contact by Email](actions/get-contact-by-email.md) | GET |  |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET |  |
| [Get Contact by Name](actions/get-contact-by-name.md) | GET |  |
| [Get Contact by Out ID](actions/get-contact-by-out-id.md) | GET |  |
| [Get Contact by Phone](actions/get-contact-by-phone.md) | GET |  |
| [Get Contact by Session ID](actions/get-contact-by-session-id.md) | GET |  |
| [Get Contact by Visitor ID](actions/get-contact-by-visitor-id.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Contacts by Ad Campaign](actions/list-contacts-by-ad-campaign.md) | GET |  |
| [List Contacts by Source](actions/list-contacts-by-source.md) | GET |  |
| [List Contacts by Traffic Channel](actions/list-contacts-by-traffic-channel.md) | GET |  |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal by ID](actions/get-deal-by-id.md) | GET |  |
| [Get Deal by Out ID](actions/get-deal-by-out-id.md) | GET |  |
| [List Deals](actions/list-deals.md) | GET |  |
| [List Deals by Budget](actions/list-deals-by-budget.md) | GET |  |
| [List Deals by Lead ID](actions/list-deals-by-lead-id.md) | GET |  |
| [List Deals by Pipeline ID](actions/list-deals-by-pipeline-id.md) | GET |  |
| [List Deals by Stage ID](actions/list-deals-by-stage-id.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET |  |

