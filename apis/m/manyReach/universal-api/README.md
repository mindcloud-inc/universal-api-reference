# <img src="https://images.mindcloud.co/apps/icons/many-reach_1774382452875.png" alt="ManyReach logo" width="28" height="28"> ManyReach: Universal API

ManyReach is a cold email outreach platform for managing prospects, campaigns, replies, and outreach automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/manyReach/latest
- **Category:** Marketing
- **Actions:** 63
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.manyreach.com/
- **Vendor API docs:** https://api.manyreach.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Mailing Lists](actions/list-mailing-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (63)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in ManyReach. |
| [Create Campaign Copy](actions/create-campaign-copy.md) | POST | Creates a copy of a campaign in ManyReach. |
| [Create Campaign Sequence](actions/create-campaign-sequence.md) | POST | Creates a sequence for a campaign in ManyReach. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from ManyReach. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from ManyReach. |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET | Retrieves campaign statistics from ManyReach. |
| [List Campaign Sequences](actions/list-campaign-sequences.md) | GET | Retrieves sequences for a campaign from ManyReach. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from ManyReach. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses a campaign in ManyReach. |
| [Remove Campaign Prospect](actions/remove-campaign-prospect.md) | DELETE | Deletes a prospect from a campaign in ManyReach. |
| [Start Campaign](actions/start-campaign.md) | PUT | Starts a campaign in ManyReach. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in ManyReach. |

### Clientspace

| Action | Method | Description |
| --- | --- | --- |
| [Delete Clientspace](actions/delete-clientspace.md) | DELETE | Deletes an existing clientspace from ManyReach. |
| [Get Clientspace](actions/get-clientspace.md) | GET | Retrieves a clientspace from ManyReach. |
| [Update Clientspace](actions/update-clientspace.md) | PUT | Updates an existing clientspace in ManyReach. |

### Clientspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Clientspaces](actions/list-clientspaces.md) | GET | Retrieves clientspaces from ManyReach. |

### Followup

| Action | Method | Description |
| --- | --- | --- |
| [Create Sequence Follow-Up](actions/create-sequence-follow-up.md) | POST | Creates a follow-up for a sequence in ManyReach. |
| [Delete Follow-Up](actions/delete-follow-up.md) | DELETE | Deletes an existing follow-up from ManyReach. |
| [Get Follow-Up](actions/get-follow-up.md) | GET | Retrieves a follow-up from ManyReach. |
| [Update Follow-Up](actions/update-follow-up.md) | PUT | Updates an existing follow-up in ManyReach. |

### Followups

| Action | Method | Description |
| --- | --- | --- |
| [List Sequence Follow-Ups](actions/list-sequence-follow-ups.md) | GET | Retrieves follow-ups for a sequence from ManyReach. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailing List](actions/create-mailing-list.md) | POST | Creates a new mailing list in ManyReach. |
| [Delete Mailing List](actions/delete-mailing-list.md) | DELETE | Deletes an existing mailing list from ManyReach. |
| [Get Mailing List](actions/get-mailing-list.md) | GET | Retrieves a mailing list from ManyReach. |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET | Retrieves mailing lists from ManyReach. |
| [Remove List Prospect](actions/remove-list-prospect.md) | DELETE | Deletes a prospect from a mailing list in ManyReach. |
| [Update Mailing List](actions/update-mailing-list.md) | PUT | Updates an existing mailing list in ManyReach. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from ManyReach. |
| [List Prospect Messages](actions/list-prospect-messages.md) | GET | Retrieves messages for a prospect from ManyReach. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Create Prospect](actions/create-prospect.md) | POST | Creates a new prospect in ManyReach. |
| [Delete Prospect](actions/delete-prospect.md) | DELETE | Deletes an existing prospect from ManyReach. |
| [Get Prospect](actions/get-prospect.md) | GET | Retrieves a prospect from ManyReach. |
| [Update Prospect](actions/update-prospect.md) | PUT | Updates an existing prospect in ManyReach. |

### Prospects

| Action | Method | Description |
| --- | --- | --- |
| [Add Prospects in Bulk](actions/add-prospects-in-bulk.md) | POST | Creates prospects in bulk in ManyReach. |
| [List Prospects](actions/list-prospects.md) | GET | Retrieves prospects from ManyReach. |
| [List Tag Prospects](actions/list-tag-prospects.md) | GET | Retrieves prospects for a tag from ManyReach. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender](actions/create-sender.md) | POST | Creates a new sender in ManyReach. |
| [Delete Sender](actions/delete-sender.md) | DELETE | Deletes an existing sender from ManyReach. |
| [Get Sender](actions/get-sender.md) | GET | Retrieves a sender from ManyReach. |
| [List Senders](actions/list-senders.md) | GET | Retrieves senders from ManyReach. |
| [Update Sender](actions/update-sender.md) | PUT | Updates an existing sender in ManyReach. |

### Sender Error

| Action | Method | Description |
| --- | --- | --- |
| [List Sender Errors](actions/list-sender-errors.md) | GET | Retrieves errors for a sender from ManyReach. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sequence](actions/delete-sequence.md) | DELETE | Deletes an existing sequence from ManyReach. |
| [Update Sequence](actions/update-sequence.md) | PUT | Updates an existing sequence in ManyReach. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in ManyReach. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from ManyReach. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from ManyReach. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in ManyReach. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Prospect Tag](actions/add-prospect-tag.md) | POST | Adds a tag to a prospect in ManyReach. |
| [List Prospect Tags](actions/list-prospect-tags.md) | GET | Retrieves tags for a prospect from ManyReach. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from ManyReach. |
| [Remove Prospect Tag](actions/remove-prospect-tag.md) | DELETE | Deletes a tag from a prospect in ManyReach. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in ManyReach. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from ManyReach. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from ManyReach. |
| [List Users](actions/list-users.md) | GET | Retrieves users from ManyReach. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in ManyReach. |

### Whitelabel

| Action | Method | Description |
| --- | --- | --- |
| [Update Whitelabel Settings](actions/update-whitelabel-settings.md) | PUT | Updates whitelabel settings in ManyReach. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in ManyReach. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from ManyReach. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from ManyReach. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from ManyReach. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in ManyReach. |

