# Sisense: Native API Reference

A consolidated summary of Sisense's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://developer.sisense.com/guides/restApi/using-rest-api.html
- **API base URL:** `https://signup-126940n0.sisense.com`

## Authentication

### API Token

Authenticate with a Sisense API token sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.sisense.com/guides/sdk/getting-started/authentication-security.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `skip` in the query string as the record offset.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Column To Table](actions/add-custom-column-to-table.md) | `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-or-removing-a-table-s-columns) |
| [Build Extract Datamodel](actions/build-extract-datamodel.md) | `POST /api/v2/builds` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#building-extract-datamodels) |
| [Cancel Build Task](actions/cancel-build-task.md) | `DELETE /api/v2/builds/:buildId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#api-structure) |
| [Cancel Build Tasks For Datamodel](actions/cancel-build-tasks-for-datamodel.md) | `DELETE /api/v2/builds` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#api-structure) |
| [Create Blank Datamodel](actions/create-blank-datamodel.md) | `POST /api/v2/datamodels` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-blank-datamodel-object) |
| [Create Dataset](actions/create-dataset.md) | `POST /api/v2/datamodels/:datamodelId/datasets` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-dataset) |
| [Create Extract Security Rules In Bulk](actions/create-extract-security-rules-in-bulk.md) | `POST /api/elasticubes/datasecurity` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints) |
| [Create Live Datamodel Security Rules](actions/create-live-datamodel-security-rules.md) | `POST /api/v1/elasticubes/live/:title/datasecurity` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints-2) |
| [Create Relation](actions/create-relation.md) | `POST /api/v2/datamodels/:datamodelId/relations` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-relation) |
| [Create Table](actions/create-table.md) | `POST /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-table) |
| [Create Viewpoint](actions/create-viewpoint.md) | `POST /api/v1/infusion/viewpoints` | [docs](https://developer.sisense.com/guides/restApi/infusion-api.html#post-infusion-viewpoints) |
| [Delete Datamodel](actions/delete-datamodel.md) | `DELETE /api/v2/datamodels/:datamodelId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-an-entire-datamodel) |
| [Delete Dataset](actions/delete-dataset.md) | `DELETE /api/v2/datamodels/:datamodelId/datasets/:datasetId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-a-dataset) |
| [Delete Live Security Rule By Id](actions/delete-live-security-rule-by-id.md) | `DELETE /api/v1/elasticubes/live/datasecurity/:dataSecurityId` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints-2) |
| [Delete Live Security Rules For A Column](actions/delete-live-security-rules-for-a-column.md) | `DELETE /api/v1/elasticubes/live/:title/datasecurity/:table/:column` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints-2) |
| [Delete Relation](actions/delete-relation.md) | `DELETE /api/v2/datamodels/:datamodelId/relations/:relationId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-relations) |
| [Delete Table](actions/delete-table.md) | `DELETE /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-a-table) |
| [Delete Table Column](actions/delete-table-column.md) | `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-a-column) |
| [Delete Viewpoint](actions/delete-viewpoint.md) | `DELETE /api/v1/infusion/viewpoints/:id` | [docs](https://developer.sisense.com/guides/restApi/infusion-api.html#delete-infusion-viewpoints-id) |
| [Get Build Task Status](actions/get-build-task-status.md) | `GET /api/v2/builds/:buildId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#building-extract-datamodels) |
| [Get Datamodel](actions/get-datamodel.md) | `GET /api/v2/datamodels/:datamodelId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [Get Dataset](actions/get-dataset.md) | `GET /api/v2/datamodels/:datamodelId/datasets/:datasetId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [Get Extract Datamodel Security Rules](actions/get-extract-datamodel-security-rules.md) | `GET /api/elasticubes/:server/:elasticube/datasecurity` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints) |
| [Get Extract Security Rules For Dimension](actions/get-extract-security-rules-for-dimension.md) | `GET /api/elasticubes/:server/:elasticube/datasecurity/:table/:column` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints) |
| [Get Relation](actions/get-relation.md) | `GET /api/v2/datamodels/:datamodelId/relations/:relationId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [Get Table](actions/get-table.md) | `GET /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [Get Viewpoint](actions/get-viewpoint.md) | `GET /api/v1/infusion/viewpoints/:id` | [docs](https://developer.sisense.com/guides/restApi/infusion-api.html#get-infusion-viewpoints-id) |
| [Hide Or Show Table Column](actions/hide-or-show-table-column.md) | `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-or-removing-a-table-s-columns) |
| [List Build Tasks](actions/list-build-tasks.md) | `GET /api/v2/builds` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#api-structure) |
| [List Datamodels](actions/list-datamodels.md) | `GET /api/v2/datamodels` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [List Datasets](actions/list-datasets.md) | `GET /api/v2/datamodels/:datamodelId/datasets` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [List Live Datamodel Security Rules](actions/list-live-datamodel-security-rules.md) | `GET /api/v1/elasticubes/live/:title/datasecurity` | [docs](https://developer.sisense.com/guides/restApi/data-security.html#endpoints-2) |
| [List Relations](actions/list-relations.md) | `GET /api/v2/datamodels/:datamodelId/relations` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [List Tables](actions/list-tables.md) | `GET /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints) |
| [List Users](actions/list-users.md) | `GET /api/v1/users` | [docs](https://developer.sisense.com/guides/restApi/using-rest-api.html) |
| [List Viewpoints](actions/list-viewpoints.md) | `GET /api/v1/infusion/viewpoints` | [docs](https://developer.sisense.com/guides/restApi/infusion-api.html#get-infusion-viewpoints) |
| [Publish Live Datamodel](actions/publish-live-datamodel.md) | `POST /api/v2/builds` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#publishing-live-datamodels) |
| [Update Dataset Connection](actions/update-dataset-connection.md) | `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#changing-a-dataset-s-connection) |
| [Update Relation](actions/update-relation.md) | `PATCH /api/v2/datamodels/:datamodelId/relations/:relationId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-relations) |
| [Update Table](actions/update-table.md) | `PATCH /api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId` | [docs](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-a-table) |
| [Update Viewpoint](actions/update-viewpoint.md) | `PUT /api/v1/infusion/viewpoints/:id` | [docs](https://developer.sisense.com/guides/restApi/infusion-api.html#put-infusion-viewpoints-id) |
