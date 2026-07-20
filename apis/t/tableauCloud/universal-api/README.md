# <img src="https://images.mindcloud.co/apps/icons/images-3_1773940003339.png" alt="Tableau Cloud logo" width="28" height="28"> Tableau Cloud: Universal API

Query and manage Tableau Cloud projects, workbooks, views, data sources, flows, favorites, and subscriptions through the Tableau REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tableauCloud/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tableau.com/
- **Vendor API docs:** https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Projects](actions/query-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Add Workbook to Favorites](actions/add-workbook-to-favorites.md) | POST | Adds a workbook to favorites in Tableau Cloud. |
| [Delete Workbook from Favorites](actions/delete-workbook-from-favorites.md) | DELETE | Deletes a workbook from favorites in Tableau Cloud. |
| [Get Favorites for User](actions/get-favorites-for-user.md) | GET | Retrieves a user's favorites from Tableau Cloud. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Query Data Source Connections](actions/query-data-source-connections.md) | GET | Retrieves data source connections from Tableau Cloud. |
| [Query Flow Connections](actions/query-flow-connections.md) | GET | Retrieves flow connections from Tableau Cloud. |
| [Query Workbook Connections](actions/query-workbook-connections.md) | GET | Retrieves workbook connections from Tableau Cloud. |
| [Update Data Source Connections](actions/update-data-source-connections.md) | PUT | Updates data source connections in Tableau Cloud. |
| [Update Workbook Connections](actions/update-workbook-connections.md) | PUT | Updates workbook connections in Tableau Cloud. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Download Data Source](actions/download-data-source.md) | GET | Downloads a data source from Tableau Cloud as TDSX. |
| [Publish Data Source](actions/publish-data-source.md) | POST | Publishes a data source to Tableau Cloud. |
| [Query Data Source](actions/query-data-source.md) | GET | Retrieves a data source from Tableau Cloud. |
| [Query Data Sources](actions/query-data-sources.md) | GET | Retrieves a list of data sources from Tableau Cloud. |
| [Update Data Source](actions/update-data-source.md) | PUT | Updates an existing data source in Tableau Cloud. |
| [Update Data Source Now](actions/update-data-source-now.md) | PUT | Refreshes a data source in Tableau Cloud. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Recently Viewed for Site](actions/get-recently-viewed-for-site.md) | GET | Retrieves recently viewed content from Tableau Cloud. |
| [Sign In](actions/sign-in.md) | GET | Signs in to Tableau Cloud and returns an auth token. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Tableau Cloud. |
| [Query Projects](actions/query-projects.md) | GET | Retrieves a list of projects from Tableau Cloud. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Tableau Cloud. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Delete Workbook](actions/delete-workbook.md) | DELETE | Deletes a workbook from Tableau Cloud. |
| [Get Workbook](actions/get-workbook.md) | GET | Retrieves a workbook from Tableau Cloud. |
| [Publish Workbook](actions/publish-workbook.md) | POST | Publishes a workbook to Tableau Cloud. |
| [Query Workbooks for Site](actions/query-workbooks-for-site.md) | GET | Retrieves site workbooks from Tableau Cloud. |
| [Query Workbooks for User](actions/query-workbooks-for-user.md) | GET | Retrieves a user's workbooks from Tableau Cloud. |
| [Update Workbook Now](actions/update-workbook-now.md) | PUT | Refreshes a workbook in Tableau Cloud. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Tableau Cloud. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Tableau Cloud. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves a list of subscriptions from Tableau Cloud. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get View](actions/get-view.md) | GET | Retrieves a view from Tableau Cloud. |
| [Query View Data](actions/query-view-data.md) | GET | Retrieves view data from Tableau Cloud as CSV. |
| [Query View Image](actions/query-view-image.md) | GET | Retrieves a view image from Tableau Cloud. |
| [Query View PDF](actions/query-view-pdf.md) | GET | Retrieves a view PDF from Tableau Cloud. |
| [Query Views for Site](actions/query-views-for-site.md) | GET | Retrieves site views from Tableau Cloud. |
| [Query Views for Workbook](actions/query-views-for-workbook.md) | GET | Retrieves workbook views from Tableau Cloud. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Flow Run](actions/get-flow-run.md) | GET | Retrieves a flow run from Tableau Cloud. |
| [Get Flow Runs](actions/get-flow-runs.md) | GET | Retrieves flow runs from Tableau Cloud. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Delete Flow](actions/delete-flow.md) | DELETE | Deletes a flow from Tableau Cloud. |
| [Publish Flow](actions/publish-flow.md) | POST | Publishes a flow to Tableau Cloud. |
| [Query Flow](actions/query-flow.md) | GET | Retrieves a flow from Tableau Cloud. |
| [Query Flows for User](actions/query-flows-for-user.md) | GET | Retrieves a user's flows from Tableau Cloud. |
| [Run Flow Now](actions/run-flow-now.md) | POST | Runs a flow in Tableau Cloud. |

