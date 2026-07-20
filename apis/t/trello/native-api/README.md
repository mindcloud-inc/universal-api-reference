# Trello: Native API Reference

A consolidated summary of Trello's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developer.atlassian.com/cloud/trello/rest/
- **API base URL:** `https://api.trello.com/1`

## Authentication

### API Key

Archives an existing list in Trello.

### Credentials

- **API Key:** `apiKey` · required
- **Token:** `token` · required

Send these headers with each API request:

```http
Authorization: OAuth oauth_consumer_key="<apiKey>", oauth_token="<token>"
```

[Official authentication documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/authorization/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Attachment to Card](actions/add-attachment-to-card.md) | `POST cards/:id/attachments` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-attachments-post) |
| [Add CheckItem to Checklist](actions/add-check-item-to-checklist.md) | `POST checklists/:id/checkItems` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-id-checkitems-post) |
| [Add Comment to Card](actions/add-comment-to-card.md) | `POST cards/:id/actions/comments` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-actions-comments-post) |
| [Add Label to Card](actions/add-label-to-card.md) | `POST cards/:id/idLabels` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idlabels-post) |
| [Add Member to Card](actions/add-member-to-card.md) | `POST cards/:id/idMembers` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idmembers-post) |
| [Archive Board](actions/archive-board.md) | `PUT boards/:id/closed` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-closed-put) |
| [Archive List](actions/archive-list.md) | `PUT lists/:id/closed` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-closed-put) |
| [Create Board](actions/create-board.md) | `POST boards` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post) |
| [Create Card](actions/create-card.md) | `POST cards` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-post) |
| [Create Checklist](actions/create-checklist.md) | `POST checklists` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-post) |
| [Create Checklist on a Card](actions/create-checklist-on-a-card.md) | `POST cards/:id/checklists` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-checklists-post) |
| [Create List on Board](actions/create-list-on-board.md) | `POST boards/:id/lists` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-lists-post) |
| [Delete Attachment from Card](actions/delete-attachment-from-card.md) | `DELETE cards/:id/attachments/:idAttachment` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-attachments-idattachment-delete) |
| [Delete Card](actions/delete-card.md) | `DELETE cards/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-delete) |
| [Delete CheckItem from Checklist](actions/delete-check-item-from-checklist.md) | `DELETE checklists/:id/checkItems/:idCheckItem` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-checklists/#api-checklists-id-checkitems-idcheckitem-delete) |
| [Get Actions on a Card](actions/get-actions-on-a-card.md) | `GET cards/:id/actions` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-actions-get) |
| [Get Attachments on a Card](actions/get-attachments-on-a-card.md) | `GET cards/:id/attachments` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-attachments-get) |
| [Get Board](actions/get-board.md) | `GET boards/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-get) |
| [Get Card](actions/get-card.md) | `GET cards/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-get) |
| [Get Cards in a List](actions/get-cards-in-a-list.md) | `GET lists/:id/cards` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-cards-get) |
| [Get Cards on a Board](actions/get-cards-on-a-board.md) | `GET boards/:id/cards` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-cards-get) |
| [Get Checklists on a Card](actions/get-checklists-on-a-card.md) | `GET cards/:id/checklists` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-checklists-get) |
| [Get List](actions/get-list.md) | `GET lists/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-get) |
| [Get Lists on a Board](actions/get-lists-on-a-board.md) | `GET boards/:id/lists` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-lists-get) |
| [Get Member](actions/get-member.md) | `GET members/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-members/#api-members-id-get) |
| [List Boards By Member](actions/list-boards-by-member.md) | `GET members/:id/boards` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-members/#api-members-id-boards-get) |
| [Remove Label from Card](actions/remove-label-from-card.md) | `DELETE cards/:id/idLabels/:idLabel` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idlabels-idlabel-delete) |
| [Remove Member from Card](actions/remove-member-from-card.md) | `DELETE cards/:id/idMembers/:idMember` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-idmembers-idmember-delete) |
| [Search Trello](actions/search-trello.md) | `GET search` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-search/#api-search-get) |
| [Update Board](actions/update-board.md) | `PUT boards/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-put) |
| [Update Card](actions/update-card.md) | `PUT cards/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-cards/#api-cards-id-put) |
| [Update List](actions/update-list.md) | `PUT lists/:id` | [docs](https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-put) |
