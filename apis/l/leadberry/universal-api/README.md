# <img src="https://images.mindcloud.co/apps/icons/leadberry_1775150476225.png" alt="Leadberry logo" width="28" height="28"> Leadberry: Universal API

Identify website visitors, capture leads, and sync them to sales tools

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadberry/latest
- **Category:** Marketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leadberry.com
- **Vendor API docs:** https://www.leadberry.com/integrations

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Websites](actions/list-websites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Alert Setting

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert Setting](actions/create-alert-setting.md) | POST |  |
| [Remove Alert Setting](actions/remove-alert-setting.md) | DELETE |  |
| [Update Alert Setting](actions/update-alert-setting.md) | PUT |  |

### Crawler Site Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Crawler Site Results](actions/get-crawler-site-results.md) | GET |  |

### Crm Additional Info

| Action | Method | Description |
| --- | --- | --- |
| [Get CRM Additional Info](actions/get-crm-additional-info.md) | GET |  |

### Crm Connection

| Action | Method | Description |
| --- | --- | --- |
| [Remove CRM Connection](actions/remove-crm-connection.md) | DELETE |  |

### Crm Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead To CRM](actions/add-lead-to-crm.md) | POST |  |

### Dashboard Csv Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Dashboard CSV](actions/export-dashboard-csv.md) | GET |  |

### Email Address Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Email Addresses](actions/download-email-addresses.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET |  |

### Lead Csv Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Leads CSV](actions/export-leads-csv.md) | GET |  |

### Lead Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Lead Email](actions/send-lead-email.md) | POST |  |

### Lead Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Leads For All Website Profile Combinations](actions/estimate-leads-for-all-website-profile-combinations.md) | GET |  |
| [Estimate Number Of Leads](actions/estimate-number-of-leads.md) | GET |  |

### Lead Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Note](actions/create-lead-note.md) | POST |  |
| [Remove Lead Note](actions/remove-lead-note.md) | DELETE |  |

### Lead Score Level

| Action | Method | Description |
| --- | --- | --- |
| [Change Lead Score Level](actions/change-lead-score-level.md) | PUT |  |

### Pabbly Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Request Pabbly API Key](actions/request-pabbly-api-key.md) | POST |  |

### Pabbly Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Remove Pabbly Webhook](actions/remove-pabbly-webhook.md) | DELETE |  |
| [Save Pabbly Webhook](actions/save-pabbly-webhook.md) | POST |  |

### Pabbly Webhook Test

| Action | Method | Description |
| --- | --- | --- |
| [Test Pabbly Webhook](actions/test-pabbly-webhook.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Added Profiles](actions/list-added-profiles.md) | GET |  |
| [Search Profiles](actions/search-profiles.md) | GET |  |

### Similar Company

| Action | Method | Description |
| --- | --- | --- |
| [Search Similar Companies](actions/search-similar-companies.md) | GET |  |

### Similar Lead Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Similar Lead Details](actions/get-similar-lead-details.md) | GET |  |

### Slack View

| Action | Method | Description |
| --- | --- | --- |
| [Save Slack View](actions/save-slack-view.md) | POST |  |

### Tracking Install Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Tracking Install](actions/check-tracking-install.md) | GET |  |

### Tracking Website

| Action | Method | Description |
| --- | --- | --- |
| [Add Tracking Website](actions/add-tracking-website.md) | POST |  |

### Url Check

| Action | Method | Description |
| --- | --- | --- |
| [Check URL Exists](actions/check-url-exists.md) | GET |  |

### User Setting

| Action | Method | Description |
| --- | --- | --- |
| [Update User Settings](actions/update-user-settings.md) | PUT |  |

### User Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get User Settings](actions/get-user-settings.md) | GET |  |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Disable Website](actions/disable-website.md) | PUT |  |
| [List Websites](actions/list-websites.md) | GET |  |
| [Whitelist Website](actions/whitelist-website.md) | PUT |  |

### Zapier Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Request Zapier API Key](actions/request-zapier-api-key.md) | POST |  |

### Zoho Grant Code

| Action | Method | Description |
| --- | --- | --- |
| [Request Zoho Grant Code](actions/request-zoho-grant-code.md) | POST |  |

