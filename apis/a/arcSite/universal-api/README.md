# <img src="https://images.mindcloud.co/apps/icons/arcsite_1774625288000.png" alt="ArcSite logo" width="28" height="28"> ArcSite: Universal API

Create drawings, manage projects, and generate proposals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/arcSite/latest
- **Category:** Support / Field Service
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.arcsite.com
- **Vendor API docs:** https://dev.arcsite.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Proposal Templates](actions/list-proposal-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/list-proposal-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Export Proposal PDF](actions/export-proposal-pdf.md) | POST | Exports a proposal PDF for an ArcSite drawing. |

### Drawing

| Action | Method | Description |
| --- | --- | --- |
| [Get Drawing](actions/get-drawing.md) | GET | Retrieves one drawing by ID from ArcSite. |
| [Import PDF to Project](actions/import-pdf-to-project.md) | POST | Imports a PDF as drawings into an ArcSite project. |
| [List Project Drawings](actions/list-project-drawings.md) | GET | Retrieves drawings for a specific ArcSite project. |

### Field Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Drawing Field Data](actions/get-drawing-field-data.md) | GET | Retrieves field data values from an ArcSite drawing. |

### Location Photo

| Action | Method | Description |
| --- | --- | --- |
| [Get Drawing Location Photos](actions/get-drawing-location-photos.md) | GET | Retrieves location photos for one ArcSite drawing. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Drawing Payment](actions/get-drawing-payment.md) | GET | Retrieves payment details for one ArcSite drawing. |
| [Get Proposal Payments](actions/get-proposal-payments.md) | GET | Retrieves received payments for a specific ArcSite proposal. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves product records from your ArcSite organization. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Collaborators](actions/add-project-collaborators.md) | PUT | Adds collaborators to an existing ArcSite project. |
| [Archive Project](actions/archive-project.md) | PUT | Archives an existing project in ArcSite. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in ArcSite. |
| [Get Project](actions/get-project.md) | GET | Retrieves one project by ID from ArcSite. |
| [List Projects](actions/list-projects.md) | GET | Retrieves project records from your ArcSite organization. |
| [Remove Project Collaborators](actions/remove-project-collaborators.md) | PUT | Removes collaborators from an existing ArcSite project. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in ArcSite using search filters. |
| [Unarchive Project](actions/unarchive-project.md) | PUT | Unarchives an existing project in ArcSite. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in ArcSite. |

### Proposal

| Action | Method | Description |
| --- | --- | --- |
| [List Proposals](actions/list-proposals.md) | GET | Retrieves proposal records from your ArcSite organization. |

### Proposal Line Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Proposal Line Items](actions/get-proposal-line-items.md) | GET | Retrieves proposal line items from an ArcSite drawing. |

### Proposal Template

| Action | Method | Description |
| --- | --- | --- |
| [List Proposal Templates](actions/list-proposal-templates.md) | GET | Retrieves proposal templates from your ArcSite organization. |

### Takeoff Line Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Takeoff Line Items](actions/get-takeoff-line-items.md) | GET | Retrieves takeoff line items from an ArcSite drawing. |

