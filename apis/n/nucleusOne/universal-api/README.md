# <img src="https://images.mindcloud.co/apps/icons/nucleus-one-dark2-1_1775563754590.png" alt="Nucleus One logo" width="28" height="28"> Nucleus One: Universal API

Access Nucleus One organizations, projects, documents, folders, tasks, comments, forms, approvals, and related workflow resources via the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nucleusOne/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nucleus.one
- **Vendor API docs:** https://client-api.nucleus.one/api/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Stats](actions/get-task-stats.md) | GET | Retrieves task statistics from a Nucleus One project. |

### Approvals

| Action | Method | Description |
| --- | --- | --- |
| [List Approvals](actions/list-approvals.md) | GET | Retrieves pending approvals from a Nucleus One project. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List Project Comments](actions/list-project-comments.md) | GET | Retrieves project comments from Nucleus One. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations available to the current Nucleus One user. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves project documents from Nucleus One. |
| [List Recently Accessed Documents](actions/list-recently-accessed-documents.md) | GET | Retrieves recently accessed documents from a Nucleus One organization. |
| [List Recycle Bin Documents](actions/list-recycle-bin-documents.md) | GET | Retrieves recycle bin documents from a Nucleus One project. |
| [Search Project Documents](actions/search-project-documents.md) | GET | Finds project documents in Nucleus One by search query. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Document Folders](actions/list-document-folders.md) | GET | Retrieves document folders from a Nucleus One project. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Form Templates](actions/list-form-templates.md) | GET | Retrieves form templates from a Nucleus One project. |
| [List Recent Document Signature Forms](actions/list-recent-document-signature-forms.md) | GET | Retrieves recent document signature forms from Nucleus One. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves project groups from Nucleus One. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Membership Package](actions/get-organization-membership-package.md) | GET | Retrieves organization membership details from Nucleus One. |
| [Get Organization Permissions](actions/get-organization-permissions.md) | GET | Retrieves organization permissions from Nucleus One. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Nucleus One. |
| [List Project Membership Packages](actions/list-project-membership-packages.md) | GET | Retrieves project memberships from a Nucleus One organization. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Nucleus One organization. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Document Subscriptions](actions/list-document-subscriptions.md) | GET | Retrieves document subscriptions from a Nucleus One project. |
| [List Task Subscriptions](actions/list-task-subscriptions.md) | GET | Retrieves task subscriptions from a Nucleus One project. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves project tags from Nucleus One. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Completed Tasks](actions/list-completed-tasks.md) | GET | Retrieves completed tasks from a Nucleus One project. |
| [List Denied Tasks](actions/list-denied-tasks.md) | GET | Retrieves denied tasks from a Nucleus One project. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from a Nucleus One project. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Settings](actions/get-project-settings.md) | GET | Retrieves project settings from Nucleus One. |
| [List Document Filter Sort Fields](actions/list-document-filter-sort-fields.md) | GET | Retrieves document filter and sort fields from Nucleus One. |
| [List Fields](actions/list-fields.md) | GET | Retrieves project fields from Nucleus One. |
| [Search Organization Content](actions/search-organization-content.md) | GET | Finds organization content in Nucleus One by search query. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves the current user profile from Nucleus One. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Nucleus One. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Processes](actions/list-processes.md) | GET | Retrieves project processes from Nucleus One. |

