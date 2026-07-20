# <img src="https://images.mindcloud.co/apps/icons/hubflo_1773863116155.png" alt="Hubflo logo" width="28" height="28"> Hubflo: Universal API

Client portal and deal workflow platform for firms managing proposals, projects, tasks, and client collaboration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hubflo/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hubflo.com
- **Vendor API docs:** https://hubflo.readme.io/reference/the-hubflo-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create Ping](actions/create-ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Hubflo. |
| [List Companies](actions/list-companies.md) | GET | Retrieves all company records from Hubflo. |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves a company from Hubflo by ID. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Hubflo. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Hubflo. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contact records from Hubflo. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Hubflo by ID. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Hubflo. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves all available organizations from Hubflo. |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Create Ping](actions/create-ping.md) | GET | Checks Hubflo API authentication with a ping. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Hubflo. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from Hubflo. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a project from Hubflo by ID. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Hubflo. |

### Proposal

| Action | Method | Description |
| --- | --- | --- |
| [Create Proposal](actions/create-proposal.md) | POST | Creates a draft proposal in Hubflo. |
| [Create Quote Item for Proposal](actions/create-quote-item-for-proposal.md) | POST | Creates a quote item for a Hubflo proposal. |
| [Issue Proposal](actions/issue-proposal.md) | POST | Issues a draft proposal in Hubflo. |
| [List Proposals](actions/list-proposals.md) | GET | Retrieves all proposal records from Hubflo. |
| [Retrieve Proposal](actions/retrieve-proposal.md) | GET | Retrieves a proposal from Hubflo by ID. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Hubflo. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all task records from Hubflo. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from Hubflo by ID. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Hubflo. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Hubflo. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves all workspace records from Hubflo. |
| [Retrieve Workspace](actions/retrieve-workspace.md) | GET | Retrieves a workspace from Hubflo by ID. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Hubflo. |

