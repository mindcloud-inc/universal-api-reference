# ArcSite: Native API Reference

A consolidated summary of ArcSite's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://dev.arcsite.com/
- **API base URL:** `https://api.arcsite.com/v1`

## Authentication

### API Token

Use an ArcSite API token from Settings > Developers > API tokens.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.arcsite.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Collaborators](actions/add-project-collaborators.md) | `POST /projects/:projectId/add_collaborators` | [docs](https://dev.arcsite.com/#add-project-collaborators) |
| [Archive Project](actions/archive-project.md) | `POST /projects/:projectId/archive` | [docs](https://dev.arcsite.com/#archive-project) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://dev.arcsite.com/#create-project) |
| [Export Proposal PDF](actions/export-proposal-pdf.md) | `POST /export_proposal_pdf` | [docs](https://dev.arcsite.com/#export-proposal-pdf) |
| [Get Drawing](actions/get-drawing.md) | `GET /drawings/:drawingId` | [docs](https://dev.arcsite.com/#get-drawing) |
| [Get Drawing Field Data](actions/get-drawing-field-data.md) | `GET /drawings/:drawingId/field_data` | [docs](https://dev.arcsite.com/#get-drawing-field-data) |
| [Get Drawing Location Photos](actions/get-drawing-location-photos.md) | `GET /drawings/:drawingId/location_photos` | [docs](https://dev.arcsite.com/#get-drawing-location-photos) |
| [Get Drawing Payment](actions/get-drawing-payment.md) | `GET /drawings/:drawingId/payment` | [docs](https://dev.arcsite.com/#get-drawing-payment) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://dev.arcsite.com/#get-project) |
| [Get Proposal Line Items](actions/get-proposal-line-items.md) | `GET /drawings/:drawingId/line_items` | [docs](https://dev.arcsite.com/#get-proposal-line-items) |
| [Get Proposal Payments](actions/get-proposal-payments.md) | `GET /proposals/:proposalId/payments` | [docs](https://dev.arcsite.com/#get-proposal-payments) |
| [Get Takeoff Line Items](actions/get-takeoff-line-items.md) | `GET /drawings/:drawingId/takeoff_items` | [docs](https://dev.arcsite.com/#get-takeoff-line-items) |
| [Import PDF to Project](actions/import-pdf-to-project.md) | `POST /projects/:projectId/import_pdf` | [docs](https://dev.arcsite.com/#import-pdf) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://dev.arcsite.com/#query-products) |
| [List Project Drawings](actions/list-project-drawings.md) | `GET /projects/:projectId/drawings` | [docs](https://dev.arcsite.com/#get-project-drawings) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://dev.arcsite.com/#query-projects) |
| [List Proposal Templates](actions/list-proposal-templates.md) | `GET /proposal_templates` | [docs](https://dev.arcsite.com/#query-proposal-templates) |
| [List Proposals](actions/list-proposals.md) | `GET /proposals` | [docs](https://dev.arcsite.com/#query-proposals) |
| [Remove Project Collaborators](actions/remove-project-collaborators.md) | `POST /projects/:projectId/remove_collaborators` | [docs](https://dev.arcsite.com/#remove-project-collaborators) |
| [Search Projects](actions/search-projects.md) | `POST /projects/search` | [docs](https://dev.arcsite.com/#search-projects) |
| [Unarchive Project](actions/unarchive-project.md) | `POST /projects/:projectId/unarchive` | [docs](https://dev.arcsite.com/#unarchive-project) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:projectId` | [docs](https://dev.arcsite.com/#update-project) |
