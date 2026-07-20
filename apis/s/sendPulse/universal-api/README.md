# <img src="https://images.mindcloud.co/apps/icons/send-pulse_1773711313461.png" alt="SendPulse logo" width="28" height="28"> SendPulse: Universal API

Manage email campaigns, mailing lists, templates, and senders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendPulse/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendpulse.com
- **Vendor API docs:** https://sendpulse.com/integrations/api/bulk-email

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in SendPulse. |
| [Get Campaign Information](actions/get-campaign-information.md) | GET | Retrieves a campaign from SendPulse by ID. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from SendPulse. |
| [List Campaigns For Mailing List](actions/list-campaigns-for-mailing-list.md) | GET | Retrieves campaigns for a SendPulse mailing list. |
| [Update Scheduled Campaign](actions/update-scheduled-campaign.md) | PUT | Updates a scheduled campaign in SendPulse. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Add Sender](actions/add-sender.md) | POST | Creates a sender address in SendPulse. |
| [List Senders](actions/list-senders.md) | GET | Retrieves a list of senders from SendPulse. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List](actions/create-mailing-list.md) | POST | Creates a new mailing list in SendPulse. |
| [Get Mailing List Campaign Cost](actions/get-mailing-list-campaign-cost.md) | GET | Retrieves campaign cost for a SendPulse mailing list. |
| [Get Mailing List Information](actions/get-mailing-list-information.md) | GET | Retrieves a mailing list from SendPulse by ID. |
| [List Mailing List Variables](actions/list-mailing-list-variables.md) | GET | Retrieves variables for a SendPulse mailing list. |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET | Retrieves a list of mailing lists from SendPulse. |
| [Update Mailing List](actions/update-mailing-list.md) | PUT | Updates an existing mailing list in SendPulse. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Emails to Mailing List](actions/add-emails-to-mailing-list.md) | POST | Creates subscribers in a SendPulse mailing list. |
| [Delete Emails From Mailing List](actions/delete-emails-from-mailing-list.md) | DELETE | Deletes subscribers from a SendPulse mailing list. |
| [Get Mailing List Contact Count](actions/get-mailing-list-contact-count.md) | GET | Retrieves the contact count for a SendPulse mailing list. |
| [List Mailing List Emails](actions/list-mailing-list-emails.md) | GET | Retrieves emails from a SendPulse mailing list. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in SendPulse. |
| [Get Template Information](actions/get-template-information.md) | GET | Retrieves a template from SendPulse by ID. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from SendPulse. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in SendPulse. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account profile information from SendPulse. |
| [Get Balance Information](actions/get-balance-information.md) | GET | Retrieves account balance information from SendPulse. |
| [Get Detailed Balance Information](actions/get-detailed-balance-information.md) | GET | Retrieves detailed account balance information from SendPulse. |

