# <img src="https://images.mindcloud.co/apps/icons/sunwise_1775766899484.png" alt="Sunwise logo" width="28" height="28"> Sunwise: Universal API

Sunwise API wrapper for solar project, proposal, and reporting workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sunwise/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sunwise.io/
- **Vendor API docs:** https://production.sunwise.ai/boty/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates or updates a contact in Sunwise. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Sunwise. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Sunwise. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Sunwise by search term. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Sunwise. |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [Get Favorite Commercial Offer](actions/get-favorite-commercial-offer.md) | GET | Retrieves a project's favorite commercial offer in Sunwise. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Projects No Files](actions/bulk-create-projects-no-files.md) | POST | Creates multiple projects without files in Sunwise. |
| [Bulk Create Projects With Files](actions/bulk-create-projects-with-files.md) | POST | Creates multiple projects from uploaded files in Sunwise. |
| [Contact Projects](actions/contact-projects.md) | GET | Retrieves projects for a contact in Sunwise. |
| [Create Project Without Consumption](actions/create-project-without-consumption.md) | POST | Creates a new project without consumption data in Sunwise. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Sunwise. |
| [Group Files](actions/group-files.md) | PUT | Groups project files for bulk creation in Sunwise. |
| [Project Search](actions/project-search.md) | GET | Finds projects in Sunwise by search term. |
| [Recent Projects](actions/recent-projects.md) | GET | Retrieves recent projects from Sunwise. |

### Proposals

| Action | Method | Description |
| --- | --- | --- |
| [Create Proposal In Project](actions/create-proposal-in-project.md) | POST | Creates a new proposal in a Sunwise project. |
| [Download Proposals Csv](actions/download-proposals-csv.md) | GET | Retrieves a proposal CSV export from Sunwise. |
| [Get Proposal](actions/get-proposal.md) | GET | Retrieves a proposal from Sunwise. |
| [Proposal Search](actions/proposal-search.md) | GET | Finds proposals in Sunwise by search term. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST | Creates a new report in Sunwise. |
| [Download Report Csv](actions/download-report-csv.md) | GET | Retrieves a report CSV export from Sunwise. |
| [Get Active Report](actions/get-active-report.md) | GET | Retrieves an active report from Sunwise. |
| [Get Active Reports](actions/get-active-reports.md) | GET | Retrieves active reports from Sunwise. |
| [Search Reports](actions/search-reports.md) | GET | Finds reports in Sunwise by search term. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Health](actions/health.md) | GET | Retrieves service health from Sunwise. |

