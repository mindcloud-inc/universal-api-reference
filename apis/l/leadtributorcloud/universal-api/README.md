# <img src="https://images.mindcloud.co/apps/icons/leadtributor512x512_1775142314671.png" alt="leadtributor.cloud logo" width="28" height="28"> leadtributor.cloud: Universal API

Manage leads, commissions, notes, forms, markets, brokerages, and attachments in leadtributor.cloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadtributorcloud/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leadtributor.cloud
- **Vendor API docs:** https://developer.leadtributor.cloud/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Access](actions/test-api-access.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/test-api-access?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Announce Lead Attachment Upload](actions/announce-lead-attachment-upload.md) | POST | Creates an attachment upload request for a lead in leadtributor.cloud. |

### Brokerage

| Action | Method | Description |
| --- | --- | --- |
| [Offer Lead On Market](actions/offer-lead-on-market.md) | POST | Creates a brokerage to offer a lead on a market in leadtributor.cloud. |

### Commission

| Action | Method | Description |
| --- | --- | --- |
| [Commission Lead](actions/commission-lead.md) | POST | Creates a commission for a lead in leadtributor.cloud. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Test API Access](actions/test-api-access.md) | GET | Retrieves an API access test result from leadtributor.cloud. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from leadtributor.cloud. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in leadtributor.cloud. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from leadtributor.cloud. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads owned by your company in leadtributor.cloud. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in leadtributor.cloud. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List All Lead Notes](actions/list-all-lead-notes.md) | GET | Retrieves notes for all leads in leadtributor.cloud. |
| [List Lead Notes](actions/list-lead-notes.md) | GET | Retrieves notes for a lead in leadtributor.cloud. |

