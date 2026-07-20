# <img src="https://images.mindcloud.co/apps/icons/kaiten_1774649360795.png" alt="Kaiten logo" width="28" height="28"> Kaiten: Universal API

Kaiten is a project management platform for spaces, boards, cards, comments, members, tags, and workflow collaboration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kaiten/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kaiten.ru/
- **Vendor API docs:** https://developers.kaiten.ru/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Current User](actions/retrieve-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Board](actions/retrieve-board.md) | GET | Retrieves a board from Kaiten. |
| [Retrieve List of Boards](actions/retrieve-list-of-boards.md) | GET | Retrieves boards from a Kaiten space. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a comment on a Kaiten card. |
| [Remove Comment](actions/remove-comment.md) | DELETE | Deletes an existing comment from Kaiten. |
| [Retrieve Card Comments](actions/retrieve-card-comments.md) | GET | Retrieves comments for a Kaiten card. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Kaiten. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Add Member to Card](actions/add-member-to-card.md) | POST | Adds a member to a Kaiten card. |
| [Remove Member from Card](actions/remove-member-from-card.md) | DELETE | Removes a member from a Kaiten card. |
| [Retrieve List of Card Members](actions/retrieve-list-of-card-members.md) | GET | Retrieves members for a Kaiten card. |
| [Update Member Role](actions/update-member-role.md) | PUT | Updates a card member role in Kaiten. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve List of Tags](actions/retrieve-list-of-tags.md) | GET | Retrieves tags from Kaiten. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag](actions/add-tag.md) | POST | Creates a tag in Kaiten. |
| [Add Tag to Card](actions/add-tag-to-card.md) | POST | Adds a tag to a Kaiten card. |
| [Remove Tag from Card](actions/remove-tag-from-card.md) | DELETE | Removes a tag from a Kaiten card. |
| [Retrieve List of Card Tags](actions/retrieve-list-of-card-tags.md) | GET | Retrieves tags for a Kaiten card. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a card in Kaiten. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from Kaiten. |
| [Retrieve Card](actions/retrieve-card.md) | GET | Retrieves a card from Kaiten. |
| [Retrieve List of Cards](actions/retrieve-list-of-cards.md) | GET | Retrieves cards from Kaiten. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in Kaiten. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Current User](actions/retrieve-current-user.md) | GET | Retrieves the current user from Kaiten. |
| [Retrieve List of Users](actions/retrieve-list-of-users.md) | GET | Retrieves users from Kaiten. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve List of Spaces](actions/retrieve-list-of-spaces.md) | GET | Retrieves spaces from Kaiten. |
| [Retrieve Space](actions/retrieve-space.md) | GET | Retrieves a space from Kaiten. |

