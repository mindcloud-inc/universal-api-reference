# <img src="https://images.mindcloud.co/apps/icons/anyleads-icon-square_1775493932985.png" alt="Anyleads logo" width="28" height="28"> Anyleads: Universal API

Anyleads provides webhook-based lead enrichment, email verification, prospecting, campaign management, and contact sync actions for sales and marketing workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anyleads/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://anyleads.com
- **Vendor API docs:** https://docs.anyleads.com/products/en

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email State](actions/verify-email-state.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/verify-email-state?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Anyleads. |

### Campaign Replies

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Replies](actions/get-campaign-replies.md) | GET | Retrieves replies for a campaign from Anyleads. |

### Campaign Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET | Retrieves statistics for a campaign from Anyleads. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Convert Company Names](actions/convert-company-names.md) | GET | Retrieves domain data for a company name from Anyleads. |
| [Enrich Company](actions/enrich-company.md) | GET | Retrieves enriched company data from Anyleads. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Anyleads. |
| [Set Contact Converted](actions/set-contact-converted.md) | PUT | Updates a contact as converted in Anyleads. |
| [Stop Sending Email To Prospect](actions/stop-sending-email-to-prospect.md) | PUT | Updates a prospect to stop receiving emails in Anyleads. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Anyleads. |
| [Update Contact Scoring](actions/update-contact-scoring.md) | PUT | Updates an existing contact's scoring in Anyleads. |

### Domain Unsubscribe

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain Unsubscribe](actions/add-domain-unsubscribe.md) | POST | Creates a domain unsubscribe entry in Anyleads. |

### Email Unsubscribe

| Action | Method | Description |
| --- | --- | --- |
| [Add Email Unsubscribe](actions/add-email-unsubscribe.md) | POST | Creates an email unsubscribe entry in Anyleads. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email State](actions/verify-email-state.md) | GET | Retrieves email verification status from Anyleads. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Find Emails By Name And Domain](actions/find-emails-by-name-and-domain.md) | GET | Finds emails in Anyleads by name and domain. |

### Lead Replies

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead Replies](actions/get-lead-replies.md) | GET | Retrieves replies for a lead from Anyleads. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Extract Emails From URLs](actions/extract-emails-from-urls.md) | GET | Retrieves emails from a website URL in Anyleads. |

