# <img src="https://images.mindcloud.co/apps/icons/go4clients_1776096998206.png" alt="Go4Clients logo" width="28" height="28"> Go4Clients: Universal API

Create campaigns, send SMS and emails, and track analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/go4Clients/latest
- **Category:** Marketing
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://go4clients.com/
- **Vendor API docs:** https://apidoc.go4clients.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### 2fa Challenge

| Action | Method | Description |
| --- | --- | --- |
| [Create 2FA Challenge](actions/create2-fa-challenge.md) | POST | Creates a two-factor authentication challenge in Go4Clients. |
| [Validate 2FA Challenge](actions/validate2-fa-challenge.md) | PUT | Validates a Go4Clients two-factor authentication code. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves plan and wallet balances from Go4Clients. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Go4Clients. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Go4Clients. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Go4Clients by search filters. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Go4Clients. |

### Email Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Email to Campaign](actions/add-email-to-campaign.md) | PUT | Adds email recipients to an existing Go4Clients campaign. |
| [Create Email Campaign](actions/create-email-campaign.md) | POST | Creates a new email campaign in Go4Clients. |
| [Get Email Campaign](actions/get-email-campaign.md) | GET | Retrieves an email campaign from Go4Clients. |
| [Update Email Campaign](actions/update-email-campaign.md) | PUT | Updates an existing email campaign in Go4Clients. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new contact group in Go4Clients. |
| [Get Group](actions/get-group.md) | GET | Retrieves a contact group from Go4Clients. |
| [List Groups](actions/list-groups.md) | GET | Retrieves contact groups from Go4Clients. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing contact group in Go4Clients. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | GET | Retrieves blacklist entries from Go4Clients. |
| [Number Lookup](actions/number-lookup.md) | GET | Retrieves phone number lookup details from Go4Clients. |
| [Search Blacklist Entries](actions/search-blacklist-entries.md) | GET | Finds blacklist entries in Go4Clients by search filters. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Pricing](actions/get-sms-pricing.md) | GET | Retrieves SMS pricing details from Go4Clients. |
| [Get Voice Pricing](actions/get-voice-pricing.md) | GET | Retrieves voice pricing details from Go4Clients. |

### Shortlink

| Action | Method | Description |
| --- | --- | --- |
| [Create Single Shortlink](actions/create-single-shortlink.md) | POST | Creates a shortlink without a campaign in Go4Clients. |

### Shortlink Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Shortlink Analytics](actions/get-shortlink-analytics.md) | GET | Retrieves shortlink campaign analytics from Go4Clients. |

### Shortlink Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Shortlink to Campaign](actions/add-shortlink-to-campaign.md) | PUT | Adds shortlinks to an existing Go4Clients campaign. |
| [Create Shortlink Campaign](actions/create-shortlink-campaign.md) | POST | Creates a new shortlink campaign in Go4Clients. |

### Voice Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Voice Analytics](actions/get-voice-analytics.md) | GET | Retrieves voice campaign analytics from Go4Clients. |

### Voice Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Calls to Voice Campaign](actions/add-calls-to-voice-campaign.md) | PUT | Adds calls to an existing Go4Clients voice campaign. |
| [Add Personalized IVR](actions/add-personalized-ivr.md) | PUT | Adds a personalized IVR to a Go4Clients voice campaign. |
| [Create Voice Campaign](actions/create-voice-campaign.md) | POST | Creates a new voice campaign in Go4Clients. |

### Voice Event

| Action | Method | Description |
| --- | --- | --- |
| [Create and Send Voice](actions/create-and-send-voice.md) | POST | Creates a campaign and sends voice calls in Go4Clients. |

