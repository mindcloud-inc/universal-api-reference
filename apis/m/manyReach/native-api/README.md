# ManyReach: Native API Reference

A consolidated summary of ManyReach's API configuration and 63 documented operations, with links to official documentation.

- **Official docs:** https://api.manyreach.com/api
- **OpenAPI specification:** https://api.manyreach.com/swagger/docs/v2
- **API base URL:** `https://api.manyreach.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.manyreach.com/en/articles/60-how-to-connect-n8n-to-manyreach-using-api-integration)

## Endpoints (63 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Prospect Tag](actions/add-prospect-tag.md) | `POST https://api.manyreach.com/api/v2/prospects/:id/tags` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Add Prospects in Bulk](actions/add-prospects-in-bulk.md) | `POST https://api.manyreach.com/api/v2/prospects/bulk` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Create Campaign](actions/create-campaign.md) | `POST https://api.manyreach.com/api/v2/campaigns` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Create Campaign Copy](actions/create-campaign-copy.md) | `POST https://api.manyreach.com/api/v2/campaigns/:id/copy` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Create Campaign Sequence](actions/create-campaign-sequence.md) | `POST https://api.manyreach.com/api/v2/campaigns/:id/sequences` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Create Mailing List](actions/create-mailing-list.md) | `POST https://api.manyreach.com/api/v2/lists` | [docs](https://api.manyreach.com/api#v2/tag/list) |
| [Create Prospect](actions/create-prospect.md) | `POST https://api.manyreach.com/api/v2/prospects` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Create Sender](actions/create-sender.md) | `POST https://api.manyreach.com/api/v2/senders` | [docs](https://api.manyreach.com/api#v2/tag/sender) |
| [Create Sequence Follow-Up](actions/create-sequence-follow-up.md) | `POST https://api.manyreach.com/api/v2/sequences/:id/followups` | [docs](https://api.manyreach.com/api#v2/tag/sequence) |
| [Create Tag](actions/create-tag.md) | `POST https://api.manyreach.com/api/v2/tags` | [docs](https://api.manyreach.com/api#v2/tag/tags) |
| [Create User](actions/create-user.md) | `POST https://api.manyreach.com/api/v2/users` | [docs](https://api.manyreach.com/api#v2/tag/user) |
| [Create Workspace](actions/create-workspace.md) | `POST https://api.manyreach.com/api/v2/workspaces` | [docs](https://api.manyreach.com/api#v2/tag/workspace) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE https://api.manyreach.com/api/v2/campaigns/:id` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Delete Clientspace](actions/delete-clientspace.md) | `DELETE https://api.manyreach.com/api/v2/clientspaces/:id` | [docs](https://api.manyreach.com/api#v2/tag/clientspace) |
| [Delete Follow-Up](actions/delete-follow-up.md) | `DELETE https://api.manyreach.com/api/v2/followups/:id` | [docs](https://api.manyreach.com/api#v2/tag/followup) |
| [Delete Mailing List](actions/delete-mailing-list.md) | `DELETE https://api.manyreach.com/api/v2/lists/:id` | [docs](https://api.manyreach.com/api#v2/tag/list) |
| [Delete Prospect](actions/delete-prospect.md) | `DELETE https://api.manyreach.com/api/v2/prospects/:id` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Delete Sender](actions/delete-sender.md) | `DELETE https://api.manyreach.com/api/v2/senders/:id` | [docs](https://api.manyreach.com/api#v2/tag/sender) |
| [Delete Sequence](actions/delete-sequence.md) | `DELETE https://api.manyreach.com/api/v2/sequences/:id` | [docs](https://api.manyreach.com/api#v2/tag/sequence) |
| [Delete Tag](actions/delete-tag.md) | `DELETE https://api.manyreach.com/api/v2/tags/:id` | [docs](https://api.manyreach.com/api#v2/tag/tags) |
| [Delete User](actions/delete-user.md) | `DELETE https://api.manyreach.com/api/v2/users/:id` | [docs](https://api.manyreach.com/api#v2/tag/user) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE https://api.manyreach.com/api/v2/workspaces/:id` | [docs](https://api.manyreach.com/api#v2/tag/workspace) |
| [Get Campaign](actions/get-campaign.md) | `GET https://api.manyreach.com/api/v2/campaigns/:id` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET https://api.manyreach.com/api/v2/campaigns/:id/stats` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Get Clientspace](actions/get-clientspace.md) | `GET https://api.manyreach.com/api/v2/clientspaces/:id` | [docs](https://api.manyreach.com/api#v2/tag/clientspace) |
| [Get Follow-Up](actions/get-follow-up.md) | `GET https://api.manyreach.com/api/v2/followups/:id` | [docs](https://api.manyreach.com/api#v2/tag/followup) |
| [Get Mailing List](actions/get-mailing-list.md) | `GET https://api.manyreach.com/api/v2/lists/:id` | [docs](https://api.manyreach.com/api#v2/tag/list) |
| [Get Prospect](actions/get-prospect.md) | `GET https://api.manyreach.com/api/v2/prospects/:id` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Get Sender](actions/get-sender.md) | `GET https://api.manyreach.com/api/v2/senders/:id` | [docs](https://api.manyreach.com/api#v2/tag/sender) |
| [Get Tag](actions/get-tag.md) | `GET https://api.manyreach.com/api/v2/tags/:id` | [docs](https://api.manyreach.com/api#v2/tag/tags) |
| [Get User](actions/get-user.md) | `GET https://api.manyreach.com/api/v2/users/:id` | [docs](https://api.manyreach.com/api#v2/tag/user) |
| [Get Workspace](actions/get-workspace.md) | `GET https://api.manyreach.com/api/v2/workspaces/:id` | [docs](https://api.manyreach.com/api#v2/tag/workspace) |
| [List Campaign Sequences](actions/list-campaign-sequences.md) | `GET https://api.manyreach.com/api/v2/campaigns/:id/sequences` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [List Campaigns](actions/list-campaigns.md) | `GET https://api.manyreach.com/api/v2/campaigns` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [List Clientspaces](actions/list-clientspaces.md) | `GET https://api.manyreach.com/api/v2/clientspaces` | [docs](https://api.manyreach.com/api#v2/tag/clientspace) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET https://api.manyreach.com/api/v2/lists` | [docs](https://api.manyreach.com/api#v2/tag/list) |
| [List Messages](actions/list-messages.md) | `GET https://api.manyreach.com/api/v2/messages` | [docs](https://api.manyreach.com/api#v2/tag/message) |
| [List Prospect Messages](actions/list-prospect-messages.md) | `GET https://api.manyreach.com/api/v2/prospects/:id/messages` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [List Prospect Tags](actions/list-prospect-tags.md) | `GET https://api.manyreach.com/api/v2/prospects/:id/tags` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [List Prospects](actions/list-prospects.md) | `GET https://api.manyreach.com/api/v2/prospects` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [List Sender Errors](actions/list-sender-errors.md) | `GET https://api.manyreach.com/api/v2/senders/:id/errors` | [docs](https://api.manyreach.com/api#v2/tag/sender) |
| [List Senders](actions/list-senders.md) | `GET https://api.manyreach.com/api/v2/senders` | [docs](https://api.manyreach.com/api#v2/tag/sender) |
| [List Sequence Follow-Ups](actions/list-sequence-follow-ups.md) | `GET https://api.manyreach.com/api/v2/sequences/:id/followups` | [docs](https://api.manyreach.com/api#v2/tag/sequence) |
| [List Tag Prospects](actions/list-tag-prospects.md) | `GET https://api.manyreach.com/api/v2/tags/:id/prospects` | [docs](https://api.manyreach.com/api#v2/tag/tags) |
| [List Tags](actions/list-tags.md) | `GET https://api.manyreach.com/api/v2/tags` | [docs](https://api.manyreach.com/api#v2/tag/tags) |
| [List Users](actions/list-users.md) | `GET https://api.manyreach.com/api/v2/users` | [docs](https://api.manyreach.com/api#v2/tag/user) |
| [List Workspaces](actions/list-workspaces.md) | `GET https://api.manyreach.com/api/v2/workspaces` | [docs](https://api.manyreach.com/api#v2/tag/workspace) |
| [Pause Campaign](actions/pause-campaign.md) | `POST https://api.manyreach.com/api/v2/campaigns/:id/pause` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Remove Campaign Prospect](actions/remove-campaign-prospect.md) | `DELETE https://api.manyreach.com/api/v2/campaigns/:id/prospects/:prospectId` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Remove List Prospect](actions/remove-list-prospect.md) | `DELETE https://api.manyreach.com/api/v2/lists/:id/prospects/:prospectId` | [docs](https://api.manyreach.com/api#v2/tag/list) |
| [Remove Prospect Tag](actions/remove-prospect-tag.md) | `DELETE https://api.manyreach.com/api/v2/prospects/:id/tags/:tagId` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Start Campaign](actions/start-campaign.md) | `POST https://api.manyreach.com/api/v2/campaigns/:id/start` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Update Campaign](actions/update-campaign.md) | `PATCH https://api.manyreach.com/api/v2/campaigns/:id` | [docs](https://api.manyreach.com/api#v2/tag/campaign) |
| [Update Clientspace](actions/update-clientspace.md) | `PATCH https://api.manyreach.com/api/v2/clientspaces/:id` | [docs](https://api.manyreach.com/api#v2/tag/clientspace) |
| [Update Follow-Up](actions/update-follow-up.md) | `PATCH https://api.manyreach.com/api/v2/followups/:id` | [docs](https://api.manyreach.com/api#v2/tag/followup) |
| [Update Mailing List](actions/update-mailing-list.md) | `PATCH https://api.manyreach.com/api/v2/lists/:id` | [docs](https://api.manyreach.com/api#v2/tag/list) |
| [Update Prospect](actions/update-prospect.md) | `PATCH https://api.manyreach.com/api/v2/prospects/:id` | [docs](https://api.manyreach.com/api#v2/tag/prospect) |
| [Update Sender](actions/update-sender.md) | `PATCH https://api.manyreach.com/api/v2/senders/:id` | [docs](https://api.manyreach.com/api#v2/tag/sender) |
| [Update Sequence](actions/update-sequence.md) | `PATCH https://api.manyreach.com/api/v2/sequences/:id` | [docs](https://api.manyreach.com/api#v2/tag/sequence) |
| [Update Tag](actions/update-tag.md) | `PATCH https://api.manyreach.com/api/v2/tags/:id` | [docs](https://api.manyreach.com/api#v2/tag/tags) |
| [Update User](actions/update-user.md) | `PATCH https://api.manyreach.com/api/v2/users/:id` | [docs](https://api.manyreach.com/api#v2/tag/user) |
| [Update Whitelabel Settings](actions/update-whitelabel-settings.md) | `PATCH https://api.manyreach.com/api/v2/whitelabel` | [docs](https://api.manyreach.com/api#v2/tag/whitelabel) |
| [Update Workspace](actions/update-workspace.md) | `PATCH https://api.manyreach.com/api/v2/workspaces/:id` | [docs](https://api.manyreach.com/api#v2/tag/workspace) |
