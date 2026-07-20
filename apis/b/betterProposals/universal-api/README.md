# <img src="https://images.mindcloud.co/apps/icons/better-proposals_1773335275658.png" alt="Better Proposals logo" width="28" height="28"> Better Proposals: Universal API

Create, send, track, and sign Better Proposals proposals and quotes from MindCloud using the official Better Proposals API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/betterProposals/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://betterproposals.io
- **Vendor API docs:** https://betterproposals.io/resources/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Settings](actions/get-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in Better Proposals. |
| [Get Company Details](actions/get-company-details.md) | GET | Retrieves company details from Better Proposals. |
| [List Companies](actions/list-companies.md) | GET | Retrieves all companies from Better Proposals. |

### Currencies

| Action | Method | Description |
| --- | --- | --- |
| [Get Currency Details](actions/get-currency-details.md) | GET | Retrieves currency details from Better Proposals. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from Better Proposals. |

### Document Types

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Type](actions/create-document-type.md) | POST | Creates a document type in Better Proposals. |
| [List Document Types](actions/list-document-types.md) | GET | Retrieves document types from Better Proposals. |

### Proposals

| Action | Method | Description |
| --- | --- | --- |
| [Create Proposal](actions/create-proposal.md) | POST | Creates a proposal in Better Proposals. |
| [Create Proposal Cover](actions/create-proposal-cover.md) | POST | Creates a proposal cover in Better Proposals. |
| [Get Proposal Details](actions/get-proposal-details.md) | GET | Retrieves proposal details from Better Proposals. |
| [List New Proposals](actions/list-new-proposals.md) | GET | Retrieves new proposals from Better Proposals. |
| [List Opened Proposals](actions/list-opened-proposals.md) | GET | Retrieves opened proposals from Better Proposals. |
| [List Proposals](actions/list-proposals.md) | GET | Retrieves all proposals from Better Proposals. |
| [List Sent Proposals](actions/list-sent-proposals.md) | GET | Retrieves sent proposals from Better Proposals. |
| [List Signed Proposals](actions/list-signed-proposals.md) | GET | Retrieves signed proposals from Better Proposals. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a quote in Better Proposals. |
| [Get Quote Details](actions/get-quote-details.md) | GET | Retrieves quote details from Better Proposals. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves all quotes from Better Proposals. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand Settings](actions/get-brand-settings.md) | GET | Retrieves brand settings from Better Proposals. |
| [Get Custom Merge Tags](actions/get-custom-merge-tags.md) | GET | Retrieves custom merge tags from Better Proposals. |
| [Get Settings](actions/get-settings.md) | GET | Retrieves account settings from Better Proposals. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Details](actions/get-template-details.md) | GET | Retrieves template details from Better Proposals. |
| [List Templates](actions/list-templates.md) | GET | Retrieves all templates from Better Proposals. |

