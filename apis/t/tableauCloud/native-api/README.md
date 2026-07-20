# Tableau Cloud: Native API Reference

A consolidated summary of Tableau Cloud's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref.htm
- **API base URL:** `https://us-east-1.online.tableau.com/api/3.28`

## Authentication

### Tableau Personal Access Token

Exchange a Tableau Cloud personal access token and site content URL for a session token used on subsequent REST API requests.

### Credentials

- **PAT Name:** `personalAccessTokenName` · required · The name of the Tableau personal access token used during sign-in.
- **PAT Secret:** `personalAccessTokenSecret` · required · The secret value shown when the Tableau personal access token is created.
- **Site Content URL:** `contentUrl` · required · The Tableau Cloud site content URL, for example MarketingSite from the browser path /#/site/MarketingSite/....

Send these headers with each API request:

```http
X-Tableau-Auth: <custom.credentials.token>
```

[Official authentication documentation](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_authentication.htm)

## Pagination

Use `pageSize` in the query string to set the page size (default 100). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Workbook to Favorites](actions/add-workbook-to-favorites.md) | `PUT /sites/site-id/favorites/user-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_favorites.htm#add_workbook_to_favorites) |
| [Create Project](actions/create-project.md) | `POST /sites/site-id/projects` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_projects.htm#create_project) |
| [Create Subscription](actions/create-subscription.md) | `POST /sites/site-id/subscriptions` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_subscriptions.htm#create_subscription) |
| [Delete Flow](actions/delete-flow.md) | `DELETE /sites/site-id/flows/flow-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#delete_flow) |
| [Delete Workbook](actions/delete-workbook.md) | `DELETE /sites/site-id/workbooks/workbook-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#delete_workbook) |
| [Delete Workbook from Favorites](actions/delete-workbook-from-favorites.md) | `DELETE /sites/site-id/favorites/user-id/workbooks/workbook-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_favorites.htm#delete_workbook_from_favorites) |
| [Download Data Source](actions/download-data-source.md) | `GET /sites/site-id/datasources/datasource-id/content` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#download_data_source) |
| [Get Favorites for User](actions/get-favorites-for-user.md) | `GET /sites/site-id/favorites/user-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_favorites.htm#get_favorites_for_user) |
| [Get Flow Run](actions/get-flow-run.md) | `GET /sites/site-id/flows/runs/flow-run-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#get_flow_run) |
| [Get Flow Runs](actions/get-flow-runs.md) | `GET /sites/site-id/flows/runs` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#get_flow_runs) |
| [Get Recently Viewed for Site](actions/get-recently-viewed-for-site.md) | `GET /sites/site-id/content/recent` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_site.htm#get_recently_viewed) |
| [Get Subscription](actions/get-subscription.md) | `GET /sites/site-id/subscriptions/subscription-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_subscriptions.htm#get_subscription) |
| [Get View](actions/get-view.md) | `GET /sites/site-id/views/view-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#get_view) |
| [Get Workbook](actions/get-workbook.md) | `GET /sites/site-id/workbooks/workbook-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_workbook) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /sites/site-id/subscriptions` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_subscriptions.htm#list_subscriptions) |
| [Publish Data Source](actions/publish-data-source.md) | `POST /sites/site-id/datasources` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_publishing.htm#publish_data_source) |
| [Publish Flow](actions/publish-flow.md) | `POST /sites/site-id/flows` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_publishing.htm#publish_flow) |
| [Publish Workbook](actions/publish-workbook.md) | `POST /sites/site-id/workbooks` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_publishing.htm#publish_workbook) |
| [Query Data Source](actions/query-data-source.md) | `GET /sites/site-id/datasources/datasource-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#query_data_source) |
| [Query Data Source Connections](actions/query-data-source-connections.md) | `GET /sites/site-id/datasources/datasource-id/connections` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#query_data_source_connections) |
| [Query Data Sources](actions/query-data-sources.md) | `GET /sites/site-id/datasources` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#query_data_sources) |
| [Query Flow](actions/query-flow.md) | `GET /sites/site-id/flows/flow-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#query_flow) |
| [Query Flow Connections](actions/query-flow-connections.md) | `GET /sites/site-id/flows/flow-id/connections` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#query_flow_connections) |
| [Query Flows for User](actions/query-flows-for-user.md) | `GET /sites/site-id/users/user-id/flows` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#query_flows_for_user) |
| [Query Projects](actions/query-projects.md) | `GET /sites/site-id/projects` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_projects.htm#query_projects) |
| [Query View Data](actions/query-view-data.md) | `GET /sites/site-id/views/view-id/data` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_view_data) |
| [Query View Image](actions/query-view-image.md) | `GET /sites/site-id/views/view-id/image` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_view_image) |
| [Query View PDF](actions/query-view-pdf.md) | `GET /sites/site-id/views/view-id/pdf` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_view_pdf) |
| [Query Views for Site](actions/query-views-for-site.md) | `GET /sites/site-id/views` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_site.htm#query_views_for_site) |
| [Query Views for Workbook](actions/query-views-for-workbook.md) | `GET /sites/site-id/workbooks/workbook-id/views` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_views_for_workbook) |
| [Query Workbook Connections](actions/query-workbook-connections.md) | `GET /sites/site-id/workbooks/workbook-id/connections` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_workbook_connections) |
| [Query Workbooks for Site](actions/query-workbooks-for-site.md) | `GET /sites/site-id/workbooks` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_workbooks_for_site) |
| [Query Workbooks for User](actions/query-workbooks-for-user.md) | `GET /sites/site-id/users/user-id/workbooks` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#query_workbooks_for_user) |
| [Run Flow Now](actions/run-flow-now.md) | `POST /sites/site-id/flows/flow-id/run` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_flow.htm#run_flow_now) |
| [Sign In](actions/sign-in.md) | `POST /auth/signin` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_authentication.htm#sign_in) |
| [Update Data Source](actions/update-data-source.md) | `PUT /sites/site-id/datasources/datasource-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#update_data_source) |
| [Update Data Source Connections](actions/update-data-source-connections.md) | `PUT /sites/site-id/datasources/datasource-id/connections` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#update_data_source_connections) |
| [Update Data Source Now](actions/update-data-source-now.md) | `POST /sites/site-id/datasources/datasource-id/refresh` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_data_sources.htm#update_data_source_now) |
| [Update Project](actions/update-project.md) | `PUT /sites/site-id/projects/project-id` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_projects.htm#update_project) |
| [Update Workbook Connections](actions/update-workbook-connections.md) | `PUT /sites/site-id/workbooks/workbook-id/connections` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#update_workbook_connections) |
| [Update Workbook Now](actions/update-workbook-now.md) | `POST /sites/site-id/workbooks/workbook-id/refresh` | [docs](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api_ref_workbooks_and_views.htm#update_workbook_now) |
