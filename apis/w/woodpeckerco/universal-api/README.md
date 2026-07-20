# <img src="https://images.mindcloud.co/apps/icons/images_1773435340863.jpeg" alt="Woodpecker.co logo" width="28" height="28"> Woodpecker.co: Universal API

Woodpecker: Manage outreach campaigns, prospects, mailboxes, and inbox replies

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/woodpeckerco/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://woodpecker.co/
- **Vendor API docs:** https://developers.woodpecker.co/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add Campaign Step](actions/add-campaign-step.md) | POST | Adds a campaign step in Woodpecker. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Woodpecker. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Woodpecker. |
| [Edit Campaign](actions/edit-campaign.md) | PUT | Makes a Woodpecker campaign editable for changes. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a single campaign from Woodpecker. |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET | Retrieves statistics for a Woodpecker campaign. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Woodpecker, optionally filtered by status. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses an active campaign in Woodpecker. |
| [Run Campaign](actions/run-campaign.md) | PUT | Starts an existing campaign in Woodpecker. |
| [Stop Campaign](actions/stop-campaign.md) | PUT | Stops an existing campaign in Woodpecker. |
| [Update Campaign Settings](actions/update-campaign-settings.md) | PUT | Updates campaign-wide settings in your Woodpecker account. |
| [Update Campaign Step](actions/update-campaign-step.md) | PUT | Updates delivery times for a Woodpecker campaign step. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Prospects To Campaign](actions/add-prospects-to-campaign.md) | POST | Adds prospects to a Woodpecker campaign. |
| [Add Prospects To Database](actions/add-prospects-to-database.md) | POST | Creates prospects in the Woodpecker database. |
| [Delete Prospects](actions/delete-prospects.md) | DELETE | Deletes prospects from Woodpecker or removes them from campaigns. |
| [List Campaign Prospects](actions/list-campaign-prospects.md) | GET | Retrieves prospects from a Woodpecker campaign. |
| [List Prospects](actions/list-prospects.md) | GET | Retrieves prospects from the Woodpecker database. |
| [Search Prospects](actions/search-prospects.md) | GET | Finds prospects in Woodpecker by search filters. |
| [Update Prospects In Campaign](actions/update-prospects-in-campaign.md) | PUT | Updates prospects in a Woodpecker campaign. |
| [Update Prospects In Database](actions/update-prospects-in-database.md) | PUT | Updates prospects in the Woodpecker database. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Add Mailboxes In Bulk](actions/add-mailboxes-in-bulk.md) | POST | Creates one or more mailboxes in Woodpecker. |
| [Get Mailbox](actions/get-mailbox.md) | GET | Retrieves a mailbox from your Woodpecker account. |
| [List Mailboxes](actions/list-mailboxes.md) | GET | Retrieves connected mailboxes from your Woodpecker account. |
| [Update Mailbox](actions/update-mailbox.md) | PUT | Updates a mailbox in your Woodpecker account. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox Messages](actions/get-inbox-messages.md) | GET | Retrieves inbox messages from the Woodpecker inbox. |
| [Get Prospect Responses](actions/get-prospect-responses.md) | GET | Retrieves responses for a Woodpecker prospect. |
| [Reply To Message](actions/reply-to-message.md) | POST | Replies to a message in the Woodpecker inbox. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Generate General Statistics Report](actions/generate-general-statistics-report.md) | POST | Generates a general campaign statistics report in Woodpecker. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Manual Tasks](actions/get-manual-tasks.md) | GET | Retrieves manual tasks from your Woodpecker account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Woodpecker. |

