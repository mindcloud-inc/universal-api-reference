# <img src="https://images.mindcloud.co/apps/icons/idk-v1e1b-i-logos_1775591273347.png" alt="Sisense logo" width="28" height="28"> Sisense: Universal API

Manage Sisense dashboards, users, and analytics data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sisense/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sisense.com
- **Vendor API docs:** https://developer.sisense.com/guides/restApi/using-rest-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Build Task

| Action | Method | Description |
| --- | --- | --- |
| [Build Extract Datamodel](actions/build-extract-datamodel.md) | POST | Starts an extract datamodel build in Sisense. |
| [Cancel Build Task](actions/cancel-build-task.md) | DELETE | Cancels an existing Sisense build task. |
| [Cancel Build Tasks For Datamodel](actions/cancel-build-tasks-for-datamodel.md) | DELETE | Cancels build tasks for a Sisense datamodel. |
| [Get Build Task Status](actions/get-build-task-status.md) | GET | Retrieves build task status from Sisense. |
| [List Build Tasks](actions/list-build-tasks.md) | GET | Retrieves build tasks from a Sisense instance. |
| [Publish Live Datamodel](actions/publish-live-datamodel.md) | POST | Publishes a live datamodel in Sisense. |

### Datamodel

| Action | Method | Description |
| --- | --- | --- |
| [Create Blank Datamodel](actions/create-blank-datamodel.md) | POST | Creates a blank datamodel in Sisense. |
| [Delete Datamodel](actions/delete-datamodel.md) | DELETE | Deletes an existing datamodel from Sisense. |
| [Get Datamodel](actions/get-datamodel.md) | GET | Retrieves a datamodel from a Sisense instance. |
| [List Datamodels](actions/list-datamodels.md) | GET | Retrieves datamodels from a Sisense instance. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Dataset](actions/create-dataset.md) | POST | Creates a dataset in a Sisense datamodel. |
| [Delete Dataset](actions/delete-dataset.md) | DELETE | Deletes an existing dataset from Sisense. |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from a Sisense datamodel. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from a Sisense datamodel. |
| [Update Dataset Connection](actions/update-dataset-connection.md) | PUT | Updates a dataset connection in Sisense. |

### Live Security Rule

| Action | Method | Description |
| --- | --- | --- |
| [Delete Live Security Rule By Id](actions/delete-live-security-rule-by-id.md) | DELETE | Deletes a live security rule from Sisense. |
| [Delete Live Security Rules For A Column](actions/delete-live-security-rules-for-a-column.md) | DELETE | Deletes live security rules for a Sisense column. |

### Relation

| Action | Method | Description |
| --- | --- | --- |
| [Create Relation](actions/create-relation.md) | POST | Creates a relation in a Sisense datamodel. |
| [Delete Relation](actions/delete-relation.md) | DELETE | Deletes an existing relation from Sisense. |
| [Get Relation](actions/get-relation.md) | GET | Retrieves a relation from a Sisense datamodel. |
| [List Relations](actions/list-relations.md) | GET | Retrieves relations from a Sisense datamodel. |
| [Update Relation](actions/update-relation.md) | PUT | Updates an existing relation in Sisense. |

### Security Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Extract Security Rules In Bulk](actions/create-extract-security-rules-in-bulk.md) | POST | Creates extract security rules in Sisense. |
| [Create Live Datamodel Security Rules](actions/create-live-datamodel-security-rules.md) | POST | Creates live datamodel security rules in Sisense. |
| [Get Extract Datamodel Security Rules](actions/get-extract-datamodel-security-rules.md) | GET | Retrieves extract datamodel security rules from Sisense. |
| [Get Extract Security Rules For Dimension](actions/get-extract-security-rules-for-dimension.md) | GET | Retrieves extract security rules for a Sisense dimension. |
| [List Live Datamodel Security Rules](actions/list-live-datamodel-security-rules.md) | GET | Retrieves live datamodel security rules from Sisense. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a table in a Sisense dataset. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes an existing table from Sisense. |
| [Get Table](actions/get-table.md) | GET | Retrieves a table from a Sisense dataset. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from a Sisense dataset. |
| [Update Table](actions/update-table.md) | PUT | Updates an existing table in Sisense. |

### Table Column

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Column To Table](actions/add-custom-column-to-table.md) | PUT | Adds a custom column to a Sisense table. |
| [Delete Table Column](actions/delete-table-column.md) | DELETE | Deletes a column from a Sisense table. |
| [Hide Or Show Table Column](actions/hide-or-show-table-column.md) | PUT | Updates a Sisense table column visibility. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Sisense instance. |

### Viewpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Viewpoint](actions/create-viewpoint.md) | POST | Creates a new viewpoint in Sisense. |
| [Delete Viewpoint](actions/delete-viewpoint.md) | DELETE | Deletes an existing viewpoint from Sisense. |
| [Get Viewpoint](actions/get-viewpoint.md) | GET | Retrieves a viewpoint from a Sisense instance. |
| [List Viewpoints](actions/list-viewpoints.md) | GET | Retrieves viewpoints from a Sisense instance. |
| [Update Viewpoint](actions/update-viewpoint.md) | PUT | Updates an existing viewpoint in Sisense. |

