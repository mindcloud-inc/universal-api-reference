# <img src="https://images.mindcloud.co/apps/icons/dataworld_1776449347416.png" alt="data.world logo" width="28" height="28"> data.world: Universal API

data.world through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataworld/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://data.world
- **Vendor API docs:** https://developer.data.world/docs/data-world-for-developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Describe a SQL Query](actions/describe-sql-query.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/describe-sql-query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Create a Dataset](actions/create-dataset.md) | POST | Creates a dataset in data.world. |
| [Delete a Dataset](actions/delete-dataset.md) | DELETE | Deletes a dataset from data.world. |
| [Download a Dataset](actions/download-dataset.md) | GET | Downloads a dataset from data.world. |
| [List Datasets for Owner](actions/list-datasets-for-owner.md) | GET | Retrieves datasets for an owner from data.world. |
| [Create / Replace a Dataset](actions/replace-dataset.md) | PUT | Creates or replaces a dataset in data.world. |
| [Retrieve Dataset](actions/retrieve-dataset.md) | GET | Retrieves a dataset from data.world. |
| [Retrieve a Dataset Version](actions/retrieve-dataset-version.md) | GET | Retrieves a dataset version from data.world. |
| [Sync Files](actions/sync-files.md) | PUT | Synchronizes dataset files in data.world. |
| [Sync Files (via GET)](actions/sync-files-via-get.md) | GET | Synchronizes dataset files in data.world using GET. |
| [Update a Dataset](actions/update-dataset.md) | PUT | Updates a dataset in data.world. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add Files from URLs](actions/add-files-from-urls.md) | POST | Adds files from URLs to a dataset in data.world. |
| [Delete Files](actions/delete-files.md) | DELETE | Deletes files from a dataset in data.world. |
| [Download a File](actions/download-file.md) | GET | Downloads a file from data.world. |
| [Get File Description and Labels](actions/get-file-metadata.md) | GET | Retrieves file descriptions and labels from data.world. |
| [Update File Description and Labels](actions/update-file-metadata.md) | PUT | Updates file descriptions and labels in data.world. |
| [Upload a File](actions/upload-file.md) | POST | Uploads a file to data.world. |
| [Upload Files](actions/upload-files.md) | POST | Uploads files to data.world. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create a Data Project](actions/create-project.md) | POST | Creates a data project in data.world. |
| [Delete a Data Project](actions/delete-project.md) | DELETE | Deletes a data project from data.world. |
| [Link Dataset](actions/link-dataset.md) | PUT | Links a dataset to a project in data.world. |
| [List Projects for Owner](actions/list-projects-for-owner.md) | GET | Retrieves projects for an owner from data.world. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a data project from data.world. |
| [Retrieve a Data Project Version](actions/retrieve-project-version.md) | GET | Retrieves a data project version from data.world. |
| [Unlink Dataset](actions/unlink-dataset.md) | DELETE | Unlinks a dataset from a project in data.world. |
| [Update a Data Project](actions/update-project.md) | PUT | Updates a data project in data.world. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Describe a SQL Query](actions/describe-sql-query.md) | GET | Describes a SQL query in data.world. |
| [Execute a Saved Query](actions/execute-saved-query.md) | GET | Executes a saved query in data.world. |
| [Execute a Saved Query (with Parameters)](actions/execute-saved-query-with-parameters.md) | GET | Executes a saved query with parameters in data.world. |
| [List User Saved Queries](actions/list-user-saved-queries.md) | GET | Retrieves user saved queries from data.world. |
| [SQL Query](actions/sql-query.md) | GET | Runs a SQL query in data.world. |

