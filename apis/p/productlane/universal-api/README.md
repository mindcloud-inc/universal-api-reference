# <img src="https://images.mindcloud.co/apps/icons/productlane_1777045502147.png" alt="Productlane logo" width="28" height="28"> Productlane: Universal API

Manage feedback, projects, and changelogs in Productlane

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productlane/latest
- **Category:** Support / Customer Success
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://productlane.com
- **Vendor API docs:** https://productlane.com/docs/integrations/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Changelog

| Action | Method | Description |
| --- | --- | --- |
| [Create Changelog](actions/create-changelog.md) | POST | Creates a new changelog in Productlane. |
| [Delete Changelog](actions/delete-changelog.md) | DELETE | Deletes an existing changelog from Productlane. |
| [Get Changelog](actions/get-changelog.md) | GET | Retrieves a changelog from your Productlane workspace. |
| [List Changelogs](actions/list-changelogs.md) | GET | Retrieves changelogs from your Productlane workspace. |
| [Update Changelog](actions/update-changelog.md) | PUT | Updates an existing changelog in Productlane. |

### Changelog Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Changelog Tags](actions/list-changelog-tags.md) | GET | Retrieves changelog tags from your Productlane workspace. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Productlane. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Productlane. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from your Productlane workspace. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from your Productlane workspace. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Productlane. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Productlane. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Productlane. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from your Productlane workspace. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Productlane workspace. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Productlane. |

### Doc Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Doc Article](actions/create-doc-article.md) | POST | Creates a help center article in Productlane. |
| [Delete Doc Article](actions/delete-doc-article.md) | DELETE | Deletes a help center article from Productlane. |
| [Get Doc Article](actions/get-doc-article.md) | GET | Retrieves a help center article from Productlane. |
| [List Doc Articles](actions/list-doc-articles.md) | GET | Retrieves help center articles from Productlane. |
| [Move Articles To Group](actions/move-articles-to-group.md) | PUT | Moves help center articles to a Productlane doc group. |
| [Update Doc Article](actions/update-doc-article.md) | PUT | Updates a help center article in Productlane. |

### Doc Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Doc Group](actions/create-doc-group.md) | POST | Creates a doc group in your Productlane help center. |
| [Delete Doc Group](actions/delete-doc-group.md) | DELETE | Deletes a doc group from your Productlane help center. |
| [Update Doc Group](actions/update-doc-group.md) | PUT | Updates a doc group in your Productlane help center. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from a Productlane portal. |
| [List Issues](actions/list-issues.md) | GET | Retrieves issues from a Productlane portal. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves workspace members from your Productlane workspace. |

### Member Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Invite User](actions/invite-user.md) | POST | Invites a user to your Productlane workspace. |

### Member Role

| Action | Method | Description |
| --- | --- | --- |
| [Update User Role](actions/update-user-role.md) | PUT | Updates a user's role in Productlane. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Creates a message in a Productlane thread. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from a Productlane portal. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Productlane portal. |

### Project Upvote

| Action | Method | Description |
| --- | --- | --- |
| [Get Upvotes](actions/get-upvotes.md) | GET | Retrieves project upvotes from the Productlane portal. |
| [Upvote Project](actions/upvote-project.md) | POST | Creates a project upvote in the Productlane portal. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Create Thread](actions/create-thread.md) | POST | Creates a new thread in Productlane. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a thread from your Productlane workspace. |
| [List Threads](actions/list-threads.md) | GET | Retrieves threads from your Productlane workspace. |
| [Update Thread](actions/update-thread.md) | PUT | Updates an existing thread in Productlane. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from your Productlane account. |

