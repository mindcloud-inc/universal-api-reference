# <img src="https://images.mindcloud.co/apps/icons/priority-matrix_1777911429693.png" alt="Priority Matrix logo" width="28" height="28"> Priority Matrix: Universal API

Manage projects, tasks, collaborators, and quadrant priorities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/priorityMatrix/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sync.appfluence.com
- **Vendor API docs:** https://sync.appfluence.com/developer/guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Priority Matrix. |

### Account Member

| Action | Method | Description |
| --- | --- | --- |
| [List Account Members](actions/list-account-members.md) | GET | Retrieves account members from Priority Matrix. |

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET | Retrieves Priority Matrix collaborators for the current user. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Comment](actions/add-item-comment.md) | POST | Creates a new comment on a Priority Matrix item. |

### Inbox Item

| Action | Method | Description |
| --- | --- | --- |
| [List Inbox Items](actions/list-inbox-items.md) | GET | Retrieves inbox items from Priority Matrix. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Item](actions/create-inbox-item.md) | POST | Creates a new inbox item in Priority Matrix. |
| [Create Project Item](actions/create-project-item.md) | POST | Creates a new item in a Priority Matrix project. |
| [Find Items By Date](actions/find-items-by-date.md) | GET | Finds Priority Matrix items by creation date. |
| [Find Items By Tag](actions/find-items-by-tag.md) | GET | Finds Priority Matrix items by tag. |
| [Get Item](actions/get-item.md) | GET | Retrieves a Priority Matrix item by ID. |
| [List Completed Project Items](actions/list-completed-project-items.md) | GET | Retrieves completed items from a Priority Matrix project. |
| [List Items](actions/list-items.md) | GET | Retrieves items from your Priority Matrix workspace. |
| [List Project Items](actions/list-project-items.md) | GET | Retrieves items from a Priority Matrix project. |
| [List Project Items By Quadrant](actions/list-project-items-by-quadrant.md) | GET | Retrieves project items from Priority Matrix by quadrant. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Priority Matrix. |
| [Update Item Notes](actions/update-item-notes.md) | PUT | Updates item notes in Priority Matrix. |

### Item Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Item Comments](actions/list-item-comments.md) | GET | Retrieves comments for a Priority Matrix item. |

### Item Follower

| Action | Method | Description |
| --- | --- | --- |
| [List Item Followers](actions/list-item-followers.md) | GET | Retrieves followers for a Priority Matrix item. |

### Item Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Project Item Summaries](actions/list-project-item-summaries.md) | GET | Retrieves item summaries from a Priority Matrix project. |

### Item Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Item Tags](actions/list-item-tags.md) | GET | Retrieves tags for a Priority Matrix item. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Priority Matrix. |
| [Find Projects By Creation Date](actions/find-projects-by-creation-date.md) | GET | Finds Priority Matrix projects by creation date. |
| [Find Projects By Schedule Date](actions/find-projects-by-schedule-date.md) | GET | Finds Priority Matrix projects by schedule date. |
| [Find Projects By Tag](actions/find-projects-by-tag.md) | GET | Finds Priority Matrix projects by tag. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Priority Matrix by IDD. |
| [List Active Projects](actions/list-active-projects.md) | GET | Retrieves active projects from Priority Matrix. |

### Project Owner

| Action | Method | Description |
| --- | --- | --- |
| [List Project Owners](actions/list-project-owners.md) | GET | Retrieves owners for a Priority Matrix project. |

### Project Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves tags for a Priority Matrix project. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Tag](actions/add-item-tag.md) | POST | Adds a tag to a Priority Matrix item. |
| [Add Project Tag](actions/add-project-tag.md) | POST | Adds a tag to a Priority Matrix project. |
| [Remove Item Tag](actions/remove-item-tag.md) | DELETE | Removes a tag from a Priority Matrix item. |
| [Remove Project Tag](actions/remove-project-tag.md) | DELETE | Removes a tag from a Priority Matrix project. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current Priority Matrix user profile. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Priority Matrix by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from Priority Matrix. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Webhook](actions/create-project-webhook.md) | POST | Creates a webhook for a Priority Matrix project. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Priority Matrix. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Priority Matrix. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhooks from Priority Matrix. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Priority Matrix. |

