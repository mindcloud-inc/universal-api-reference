# Ziflow: Native API Reference

A consolidated summary of Ziflow's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.ziflow.com/
- **OpenAPI specification:** https://api-docs.ziflow.com/data/openapi.json
- **API base URL:** `https://api.ziflow.io/v1`

## Authentication

### API Key (Header)

Authenticate to Ziflow by sending your API key in the request header `apikey`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://help.ziflow.com/hc/en-us/articles/30725093302804-How-Do-I-View-and-Edit-My-Profile)

## Pagination

Use `count` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to navigate pages; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Proof Summary PDF](actions/export-proof-summary-pdf.md) | `GET /proofs/:id/summary/pdf` | [docs](https://api-docs.ziflow.com/) |
| [Generate Folder URL](actions/generate-folder-url.md) | `GET /folders/:id/folder-url` | [docs](https://api-docs.ziflow.com/) |
| [Get Comment Label](actions/get-comment-label.md) | `GET /comment-labels/:labelId` | [docs](https://api-docs.ziflow.com/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:identifier` | [docs](https://api-docs.ziflow.com/) |
| [Get Decision Checklist Option](actions/get-decision-checklist-option.md) | `GET /decision-checklist/options/:optionId` | [docs](https://api-docs.ziflow.com/) |
| [Get Decision Reason Option](actions/get-decision-reason-option.md) | `GET /decision-reasons/options/:optionId` | [docs](https://api-docs.ziflow.com/) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:id` | [docs](https://api-docs.ziflow.com/) |
| [Get Proof](actions/get-proof.md) | `GET /proofs/:id` | [docs](https://api-docs.ziflow.com/) |
| [Get Proof Comment](actions/get-proof-comment.md) | `GET /proofs/:id/comments/:commentId` | [docs](https://api-docs.ziflow.com/) |
| [Get Proof Reviewer URL](actions/get-proof-reviewer-url.md) | `GET /proofs/:id/proof-url` | [docs](https://api-docs.ziflow.com/) |
| [Get User](actions/get-user.md) | `GET /users/:identifier` | [docs](https://api-docs.ziflow.com/) |
| [Get Workflow Template](actions/get-workflow-template.md) | `GET /workflowtemplates/:templateId` | [docs](https://api-docs.ziflow.com/) |
| [List Comment Labels](actions/list-comment-labels.md) | `GET /comment-labels` | [docs](https://api-docs.ziflow.com/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api-docs.ziflow.com/) |
| [List Decision Checklist](actions/list-decision-checklist.md) | `GET /decision-checklist` | [docs](https://api-docs.ziflow.com/) |
| [List Decision Reasons](actions/list-decision-reasons.md) | `GET /decision-reasons` | [docs](https://api-docs.ziflow.com/) |
| [List Intake Forms](actions/list-intake-forms.md) | `GET /intake-forms` | [docs](https://api-docs.ziflow.com/) |
| [List Integration Connections](actions/list-integration-connections.md) | `GET /integrations/:applicationKey/connections` | [docs](https://api-docs.ziflow.com/) |
| [List Integration Property Group Properties](actions/list-integration-property-group-properties.md) | `GET /integrations/:applicationKey/property-groups/:key/properties` | [docs](https://api-docs.ziflow.com/) |
| [List Integration Property Groups](actions/list-integration-property-groups.md) | `GET /integrations/:applicationKey/property-groups` | [docs](https://api-docs.ziflow.com/) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://api-docs.ziflow.com/) |
| [List Proof Activities](actions/list-proof-activities.md) | `GET /proofs/:id/activities` | [docs](https://api-docs.ziflow.com/) |
| [List Proof Comments](actions/list-proof-comments.md) | `GET /proofs/:id/comments` | [docs](https://api-docs.ziflow.com/) |
| [List Proof Custom Property Groups](actions/list-proof-custom-property-groups.md) | `GET /custom-properties/proofs/groups` | [docs](https://api-docs.ziflow.com/) |
| [List Proof Emails](actions/list-proof-emails.md) | `GET /proofs/:id/emails` | [docs](https://api-docs.ziflow.com/) |
| [List Proofs](actions/list-proofs.md) | `GET /proofs` | [docs](https://api-docs.ziflow.com/) |
| [List Root Folders](actions/list-root-folders.md) | `GET /folders` | [docs](https://api-docs.ziflow.com/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api-docs.ziflow.com/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://api-docs.ziflow.com/) |
| [List Workflow Templates](actions/list-workflow-templates.md) | `GET /workflowtemplates` | [docs](https://api-docs.ziflow.com/) |
