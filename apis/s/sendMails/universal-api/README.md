# <img src="https://images.mindcloud.co/apps/icons/cropped-send-mails-icon-1_1774534875050.png" alt="SendMails logo" width="28" height="28"> SendMails: Universal API

Email marketing and automation platform for managing lists, campaigns, subscribers, and contact growth.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendMails/latest
- **Category:** Communication / Email Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendmails.io/
- **Vendor API docs:** https://sendmails.io/docs/campaigns-apis-by-sendmails-io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Lists](actions/get-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/get-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in SendMails. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from SendMails. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from SendMails by ID. |
| [Get Campaigns](actions/get-campaigns.md) | GET | Retrieves a list of campaigns from SendMails. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses a campaign in SendMails. |
| [Resume Campaign](actions/resume-campaign.md) | PUT | Resumes a campaign in SendMails. |
| [Run Campaign](actions/run-campaign.md) | PUT | Runs a campaign in SendMails. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in SendMails. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File By Url](actions/upload-file-by-url.md) | POST | Uploads a file to SendMails from a URL. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in SendMails. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from SendMails. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from SendMails by ID. |
| [Get Lists](actions/get-lists.md) | GET | Retrieves a list of lists from SendMails. |

### Listfield

| Action | Method | Description |
| --- | --- | --- |
| [Add List Field](actions/add-list-field.md) | POST | Adds a custom field to a list in SendMails. |

### Logintoken

| Action | Method | Description |
| --- | --- | --- |
| [Get Login Token](actions/get-login-token.md) | POST | Generates a one-time login token in SendMails. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Tags](actions/add-subscriber-tags.md) | PUT | Adds tags to a subscriber in SendMails. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in SendMails. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from SendMails. |
| [Find Subscribers By Email](actions/find-subscribers-by-email.md) | GET | Finds subscribers in SendMails by email address. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from SendMails by ID. |
| [Get Subscribers](actions/get-subscribers.md) | GET | Retrieves a list of subscribers from SendMails. |
| [Subscribe Subscriber](actions/subscribe-subscriber.md) | PUT | Subscribes a subscriber to a list in SendMails. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Unsubscribes a subscriber from a list in SendMails. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in SendMails. |

