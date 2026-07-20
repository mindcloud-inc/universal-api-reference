# <img src="https://images.mindcloud.co/apps/icons/resco-cloud_1777486873221.png" alt="Resco Cloud logo" width="28" height="28"> Resco Cloud: Universal API

Access Resco Cloud REST and OData APIs to read metadata, query records, manage generic entity records, run server-side operations, and retrieve questionnaire data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rescoCloud/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.resco.net/
- **Vendor API docs:** https://docs.resco.net/wiki/Resco_CRM_Connector

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Who Am I](actions/who-am-i.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get OData Metadata](actions/get-o-data-metadata.md) | GET | Retrieves OData metadata from Resco Cloud. |
| [List OData Entity Sets](actions/list-o-data-entity-sets.md) | GET | Retrieves OData entity sets from Resco Cloud. |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Export Organization Data](actions/export-organization-data.md) | GET | Exports organization data and metadata from Resco Cloud. |
| [Export Project](actions/export-project.md) | GET | Exports an app project definition from Resco Cloud. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [List Questionnaire Results](actions/list-questionnaire-results.md) | GET | Retrieves questionnaire results from Resco Cloud. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Questionnaire Metadata](actions/get-questionnaire-metadata.md) | GET | Retrieves questionnaire OData metadata from Resco Cloud. |
| [List Questionnaire Templates](actions/list-questionnaire-templates.md) | GET | Retrieves questionnaire templates from Resco Cloud. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Generate Report](actions/generate-report.md) | POST | Generates a mobile report in Resco Cloud. |

### Request For Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Execute Multiple Requests](actions/execute-multiple-requests.md) | POST | Executes multiple data operations in Resco Cloud. |
| [Execute Request](actions/execute-request.md) | POST | Executes a data operation in Resco Cloud. |

### Sync States

| Action | Method | Description |
| --- | --- | --- |
| [Get Max Row Version](actions/get-max-row-version.md) | GET | Retrieves the maximum database row version from Resco Cloud. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple Records](actions/create-multiple-records.md) | POST | Creates multiple records in Resco Cloud. |
| [Create Record](actions/create-record.md) | POST | Creates a record in Resco Cloud. |
| [Delete Multiple Records](actions/delete-multiple-records.md) | DELETE | Deletes multiple records from Resco Cloud. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from Resco Cloud. |
| [Fetch Records](actions/fetch-records.md) | GET | Retrieves records from Resco Cloud using a Fetch query. |
| [Get Record Count](actions/get-record-count.md) | GET | Retrieves entity record counts from Resco Cloud. |
| [List OData Entity Records](actions/list-o-data-entity-records.md) | GET | Retrieves OData entity records from Resco Cloud. |
| [Select Records](actions/select-records.md) | GET | Retrieves entity records from Resco Cloud. |
| [Update Multiple Records](actions/update-multiple-records.md) | PUT | Updates multiple records in Resco Cloud. |
| [Update Record](actions/update-record.md) | PUT | Updates a record in Resco Cloud. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Who Am I](actions/who-am-i.md) | GET | Retrieves the current organization and user IDs from Resco Cloud. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create OData Webhook](actions/create-o-data-webhook.md) | POST | Creates an OData webhook in Resco Cloud. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Execute Workflow](actions/execute-workflow.md) | POST | Starts a workflow in Resco Cloud. |

