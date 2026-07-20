# <img src="https://images.mindcloud.co/apps/icons/images-14_1774634264416.png" alt="Emelia logo" width="28" height="28"> Emelia: Universal API

Automate prospecting campaigns, find leads, and warm up email accounts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emelia/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emelia.io
- **Vendor API docs:** https://docs-old.emelia.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Data](actions/get-user-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-user-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Emelia. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Emelia by ID. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaign listings from Emelia. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses a campaign in Emelia. |
| [Start Campaign](actions/start-campaign.md) | PUT | Starts a campaign in Emelia. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Campaign](actions/add-contact-to-campaign.md) | POST | Adds a contact to a campaign in Emelia. |
| [Add Contact To List](actions/add-contact-to-list.md) | POST | Adds a contact to a list in Emelia. |
| [Remove Contact From Campaign](actions/remove-contact-from-campaign.md) | DELETE | Deletes a contact from an Emelia campaign by email. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Emelia. |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential](actions/create-credential.md) | POST | Creates LinkedIn scraper credentials in Emelia. |
| [List Credentials](actions/list-credentials.md) | GET | Retrieves scraper credentials from Emelia. |
| [Update Credential](actions/update-credential.md) | PUT | Updates LinkedIn scraper credentials in Emelia. |

### Scrap

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook To Scrap](actions/add-webhook-to-scrap.md) | PUT | Adds a webhook to a scrap in Emelia. |
| [Download Scrap](actions/download-scrap.md) | GET | Retrieves a scrap download from Emelia. |
| [Launch Scrap](actions/launch-scrap.md) | POST | Creates a scrap in Emelia from a Sales Navigator URL. |
| [List Scraps](actions/list-scraps.md) | GET | Retrieves scrap listings from Emelia. |
| [Pause Scrap](actions/pause-scrap.md) | PUT | Pauses a segmented scrap in Emelia. |
| [Remove Webhook From Scrap](actions/remove-webhook-from-scrap.md) | DELETE | Deletes a webhook from a scrap in Emelia. |
| [Resume Scrap](actions/resume-scrap.md) | PUT | Resumes a paused scrap in Emelia. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves user account data from Emelia. |

