# <img src="https://images.mindcloud.co/apps/icons/apple-touch-icon_1774885031284.png" alt="Superthread logo" width="28" height="28"> Superthread: Universal API

Project management for engineering and product teams with spaces, boards, pages, notes, comments, projects, and sprints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/superthread/latest
- **Category:** Productivity / Project Management
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://superthread.com
- **Vendor API docs:** https://superthread.com/docs/api-docs/auth

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Account](actions/get-my-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get My Account](actions/get-my-account.md) | GET |  |
| [Update My Account](actions/update-my-account.md) | PUT |  |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | POST |  |
| [Get Board](actions/get-board.md) | GET |  |
| [List Boards](actions/list-boards.md) | GET |  |
| [Update Board](actions/update-board.md) | PUT |  |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Archive Card](actions/archive-card.md) | PUT |  |
| [Create Card](actions/create-card.md) | POST |  |
| [Get Card](actions/get-card.md) | GET |  |
| [Replace Card Description](actions/replace-card-description.md) | PUT |  |
| [Update Card Property](actions/update-card-property.md) | PUT |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Get Comment](actions/get-comment.md) | GET |  |
| [List Comments for a Resource](actions/list-comments-for-a-resource.md) | GET |  |
| [Reply to Comment](actions/reply-to-comment.md) | POST |  |

### Comment Reply

| Action | Method | Description |
| --- | --- | --- |
| [List Replies to a Comment](actions/list-replies-to-a-comment.md) | GET |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Update List](actions/update-list.md) | PUT |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Get Note](actions/get-note.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST |  |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |
| [Replace Page Content](actions/replace-page-content.md) | PUT |  |
| [Update Page Property](actions/update-page-property.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Archive Project](actions/archive-project.md) | PUT |  |
| [Create Project](actions/create-project.md) | POST |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Results](actions/search-results.md) | GET |  |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Add Member to Space](actions/add-member-to-space.md) | PUT |  |
| [Create Space](actions/create-space.md) | POST |  |
| [Get Space](actions/get-space.md) | GET |  |
| [List Spaces](actions/list-spaces.md) | GET |  |
| [Update Space](actions/update-space.md) | PUT |  |

### Sprint

| Action | Method | Description |
| --- | --- | --- |
| [Create Sprint](actions/create-sprint.md) | POST |  |
| [Get Sprint](actions/get-sprint.md) | GET |  |
| [List Sprints](actions/list-sprints.md) | GET |  |

### Sprint Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Sprint Settings](actions/get-sprint-settings.md) | GET |  |

