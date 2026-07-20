# Resco Cloud: Native API Reference

A consolidated summary of Resco Cloud's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.resco.net/wiki/Resco_CRM_Connector
- **REST API base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **REST API base URL:** `https://{organization}.app.resco.net/odata/v4`
- **REST API base URL:** `https://{organization}.app.resco.net/odata/questionnaires/v4`

## Authentication

### Organization Username & Password

Authenticate with a Resco Cloud organization, username, and password using HTTP Basic authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Organization:** `organization` · required · Resco Cloud organization subdomain, for example my_org in https://my_org.app.resco.net.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.resco.net/wiki/Resco_CRM_Connector)

## API conventions

### REST API

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml` |
| `Content-Type` | `application/xml; charset=utf-8` |

Responses from this API use XML.

### REST API

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

### REST API

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST API:** Use `$top` in the query string to set the page size (default 100; accepted range 1–5000). Use `$skip` in the query string as the record offset; numbering starts at 0.
- **REST API:** Use `$top` in the query string to set the page size (default 100; accepted range 1–1000). Use `$skip` in the query string as the record offset; numbering starts at 0.
- **REST API:** Use `$top` in the query string to set the page size (default 100; accepted range 1–1000). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

- **REST API:** Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.
- **REST API:** Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.
- **REST API:** Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

- **REST API:** Set the sort field with `$orderby` in the query string. Only one sort field is accepted.
- **REST API:** Set the sort field with `$orderby` in the query string. Only one sort field is accepted.
- **REST API:** Set the sort field with `$orderby` in the query string. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Multiple Records](actions/create-multiple-records.md) | `POST /CreateMultiple` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Create OData Webhook](actions/create-o-data-webhook.md) | `POST https://{{credentials.organization}}.rescocrm.com/odata/v4/$hook` | [docs](https://docs.resco.net/wiki/OData_service) |
| [Create Record](actions/create-record.md) | `POST /Create` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Delete Multiple Records](actions/delete-multiple-records.md) | `POST /DeleteMultiple` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Delete Record](actions/delete-record.md) | `POST /Delete` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Execute Multiple Requests](actions/execute-multiple-requests.md) | `POST /ExecuteMultiple` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Execute Request](actions/execute-request.md) | `POST /Execute` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Execute Workflow](actions/execute-workflow.md) | `POST /ExecuteWorkflow` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Export Organization Data](actions/export-organization-data.md) | `POST /Export` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Export Project](actions/export-project.md) | `POST /ExportProject` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Fetch Records](actions/fetch-records.md) | `POST` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Generate Report](actions/generate-report.md) | `POST /GenerateReport` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Get Max Row Version](actions/get-max-row-version.md) | `POST /GetMaxRowVersion` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Get OData Metadata](actions/get-o-data-metadata.md) | `GET https://{{credentials.organization}}.rescocrm.com/odata/v4/$metadata` | [docs](https://docs.resco.net/wiki/OData_service) |
| [Get Questionnaire Metadata](actions/get-questionnaire-metadata.md) | `GET https://{{credentials.organization}}.rescocrm.com/odata/questionnaires/v4/$metadata` | [docs](https://docs.resco.net/wiki/Questionnaire_OData_service) |
| [Get Record Count](actions/get-record-count.md) | `POST /GetRecordCount` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [List OData Entity Records](actions/list-o-data-entity-records.md) | `GET https://{{credentials.organization}}.rescocrm.com/odata/v4/:entity` | [docs](https://docs.resco.net/wiki/OData_service) |
| [List OData Entity Sets](actions/list-o-data-entity-sets.md) | `GET https://{{credentials.organization}}.rescocrm.com/odata/v4/` | [docs](https://docs.resco.net/wiki/OData_service) |
| [List Questionnaire Results](actions/list-questionnaire-results.md) | `GET https://{{credentials.organization}}.rescocrm.com/odata/questionnaires/v4/:template` | [docs](https://docs.resco.net/wiki/Questionnaire_OData_service) |
| [List Questionnaire Templates](actions/list-questionnaire-templates.md) | `GET https://{{credentials.organization}}.rescocrm.com/odata/questionnaires/v4/` | [docs](https://docs.resco.net/wiki/Questionnaire_OData_service) |
| [Select Records](actions/select-records.md) | `GET /:entity` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Update Multiple Records](actions/update-multiple-records.md) | `POST /UpdateMultiple` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Update Record](actions/update-record.md) | `POST /Update` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
| [Who Am I](actions/who-am-i.md) | `POST /WhoAmI` | [docs](https://docs.resco.net/wiki/Resco_CRM_Connector) |
