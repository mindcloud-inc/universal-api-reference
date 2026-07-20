# <img src="https://images.mindcloud.co/apps/icons/g-mass_1774631227427.png" alt="GMass logo" width="28" height="28"> GMass: Universal API

Create campaigns, manage lists, and track email engagement

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gMass/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gmass.co
- **Vendor API docs:** https://api.gmass.co/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a GMass campaign and its aggregate statistics. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves GMass campaigns and their aggregate statistics. |
| [List Campaigns For Zapier](actions/list-campaigns-for-zapier.md) | GET | Retrieves GMass campaigns available for Zapier. |
| [Send Campaign From Draft](actions/send-campaign-from-draft.md) | POST | Creates and sends a GMass campaign from a draft. |

### Campaign Block

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Blocks](actions/list-campaign-blocks.md) | GET | Retrieves blocked recipients from a GMass campaign. |

### Campaign Bounce

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Bounces](actions/list-campaign-bounces.md) | GET | Retrieves recipients whose emails bounced in a GMass campaign. |

### Campaign Click

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Clicks](actions/list-campaign-clicks.md) | GET | Retrieves recipients who clicked links in a GMass campaign. |

### Campaign Draft

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign Draft](actions/create-campaign-draft.md) | POST | Creates a Gmail draft for a GMass campaign. |

### Campaign Open

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Opens](actions/list-campaign-opens.md) | GET | Retrieves recipients who opened a GMass campaign. |

### Campaign Recipient

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | GET | Retrieves recipients from a GMass campaign. |

### Campaign Reply

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Replies](actions/list-campaign-replies.md) | GET | Retrieves recipients who replied to a GMass campaign. |

### Campaign Unsubscribe

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Unsubscribes](actions/list-campaign-unsubscribes.md) | GET | Retrieves recipients who unsubscribed from a GMass campaign. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Email](actions/send-transactional-email.md) | POST | Sends a transactional email through GMass. |

### Google Sheet

| Action | Method | Description |
| --- | --- | --- |
| [List Google Sheets](actions/list-google-sheets.md) | GET | Retrieves Google Sheets connected to GMass. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create Email List](actions/create-email-list.md) | POST | Creates an email list in GMass. |
| [List Email Lists](actions/list-email-lists.md) | GET | Retrieves email lists from your GMass account. |

### Sample Bounce

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Bounces](actions/list-sample-bounces.md) | GET | Retrieves sample bounces from your GMass account. |

### Sample Click

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Clicks](actions/list-sample-clicks.md) | GET | Retrieves sample clicks from your GMass account. |

### Sample Open

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Opens](actions/list-sample-opens.md) | GET | Retrieves sample opens from your GMass account. |

### Sample Reply

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Replies](actions/list-sample-replies.md) | GET | Retrieves sample replies from your GMass account. |

### Sample Unsubscribe

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Unsubscribes](actions/list-sample-unsubscribes.md) | GET | Retrieves sample unsubscribes from your GMass account. |

### Unsubscribe

| Action | Method | Description |
| --- | --- | --- |
| [Add Account Unsubscribe](actions/add-account-unsubscribe.md) | POST | Adds an address to your GMass unsubscribe list. |
| [Add Campaign Unsubscribe](actions/add-campaign-unsubscribe.md) | POST | Suppresses an email address for a GMass campaign. |
| [Remove Account Unsubscribe](actions/remove-account-unsubscribe.md) | DELETE | Deletes an address from your GMass unsubscribe list. |

### Unsubscribed Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Unsubscribed Domain](actions/add-unsubscribed-domain.md) | POST | Unsubscribes a domain from your GMass account. |
| [List Unsubscribed Domains](actions/list-unsubscribed-domains.md) | GET | Retrieves unsubscribed domains from your GMass account. |
| [Remove Unsubscribed Domain](actions/remove-unsubscribed-domain.md) | DELETE | Deletes an unsubscribed domain from GMass. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves your current GMass account information. |

### Warmup Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Warmup Stats](actions/get-warmup-stats.md) | GET | Retrieves warmup stats for your GMass account. |

### Worksheet

| Action | Method | Description |
| --- | --- | --- |
| [List Sheet Worksheets](actions/list-sheet-worksheets.md) | GET | Retrieves worksheets from a connected Google Sheet in GMass. |

