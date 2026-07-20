# Xano: Native API Reference

A consolidated summary of Xano's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.xano.com/xano-features/metadata-api
- **OpenAPI specification:** https://x8ki-letl-twmt.n7.xano.io/apispec:meta?type=json
- **API base URL:** `https://x8ki-letl-twmt.n7.xano.io`

## Authentication

### Metadata Access Token

Use a Xano Metadata API access token. Requests send the token as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.xano.com/xano-features/metadata-api)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create API](actions/create-api.md) | `POST /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_api_endpoint_using_xanoscript) |
| [Create API Group](actions/create-api-group.md) | `POST /api%3Ameta/workspace/:workspace_id/apigroup` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_api_group_in_a_workspace_include_name_description_and_optional_tags) |
| [Create Branch](actions/create-branch.md) | `POST /api%3Ameta/workspace/:workspace_id/branch` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_branch_by_cloning_an_existing_branch) |
| [Create Table](actions/create-table.md) | `POST /api%3Ameta/workspace/:workspace_id/table` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Create Table Record](actions/create-table-record.md) | `POST /api%3Ameta/workspace/:workspace_id/table/:table_id/content` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Create Workspace](actions/create-workspace.md) | `POST /api%3Ameta/workspace` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_workspace) |
| [Delete API](actions/delete-api.md) | `DELETE /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_an_api_endpoint_permanently_this_action_cannot_be_undone) |
| [Delete API Group](actions/delete-api-group.md) | `DELETE /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_an_api_group_and_all_its_endpoints_this_action_cannot_be_undone) |
| [Delete Branch](actions/delete-branch.md) | `DELETE /api%3Ameta/workspace/:workspace_id/branch/:branch_label` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_a_workspace_branch_cannot_delete_the_default_branch_or_currently_live_branch) |
| [Delete Table](actions/delete-table.md) | `DELETE /api%3Ameta/workspace/:workspace_id/table/:table_id` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Delete Table Record](actions/delete-table-record.md) | `DELETE /api%3Ameta/workspace/:workspace_id/table/:table_id/content/:content_id` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /api%3Ameta/workspace/:workspace_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_a_workspace_permanently) |
| [Get API](actions/get-api.md) | `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_a_specific_api_endpoint_by_id) |
| [Get API Group](actions/get-api-group.md) | `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/get_detailed_information_for_a_specific_api_group_returns_complete_metadata_and_configuration) |
| [Get API Group OpenAPI](actions/get-api-group-openapi.md) | `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/openapi` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/get_the_openapi_specification_for_an_api_group_returns_the_complete_swagger_json_for_all_endpoints) |
| [Get API OpenAPI](actions/get-api-openapi.md) | `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id/openapi` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/generate_openapi_specification_for_a_specific_api_endpoint) |
| [Get Branch](actions/get-branch.md) | `GET /api%3Ameta/workspace/:workspace_id/branch/:branch_label` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_a_specific_branch_by_label) |
| [Get Current User](actions/get-current-user.md) | `GET /api%3Ameta/auth/me` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_information_about_the_authenticated_user_including_id_name_and_email_address) |
| [Get Table](actions/get-table.md) | `GET /api%3Ameta/workspace/:workspace_id/table/:table_id` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Get Table Record](actions/get-table-record.md) | `GET /api%3Ameta/workspace/:workspace_id/table/:table_id/content/:content_id` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Get Workspace](actions/get-workspace.md) | `GET /api%3Ameta/workspace/:workspace_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_detailed_information_about_a_specific_workspace) |
| [List API Groups](actions/list-api-groups.md) | `GET /api%3Ameta/workspace/:workspace_id/apigroup` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_a_list_of_api_groups_inside_of_a_workspace_use_the_optional_filtering_and_sorting_parameters_for_more_granular_returns) |
| [List APIs](actions/list-apis.md) | `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_all_api_endpoints_in_a_group) |
| [List Branches](actions/list-branches.md) | `GET /api%3Ameta/workspace/:workspace_id/branch` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_all_branches_in_a_workspace) |
| [List Table Records](actions/list-table-records.md) | `GET /api%3Ameta/workspace/:workspace_id/table/:table_id/content` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [List Tables](actions/list-tables.md) | `GET /api%3Ameta/workspace/:workspace_id/table` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api%3Ameta/workspace` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_all_accessible_workspaces_for_the_authenticated_user) |
| [Search Table Records](actions/search-table-records.md) | `POST /api%3Ameta/workspace/:workspace_id/table/:table_id/content/search` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Set Live Branch](actions/set-live-branch.md) | `POST /api%3Ameta/workspace/:workspace_id/branch/:branch_label/live` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/set_a_branch_as_the_live_active_branch_for_the_workspace) |
| [Update API](actions/update-api.md) | `PUT /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/update_api_endpoint_code_settings_and_authentication_rules) |
| [Update API Group](actions/update-api-group.md) | `PUT /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/update_an_existing_api_group_modify_name_description_documentation_settings_or_tags) |
| [Update Branch](actions/update-branch.md) | `PUT /api%3Ameta/workspace/:workspace_id/branch/:branch_label` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/update_an_existing_branchs_label_description_or_color) |
| [Update Table](actions/update-table.md) | `PUT /api%3Ameta/workspace/:workspace_id/table/:table_id` | [docs](https://docs.xano.com/xano-features/metadata-api/tables-and-schema) |
| [Update Workspace](actions/update-workspace.md) | `PUT /api%3Ameta/workspace/:workspace_id` | [docs](https://docs.xano.com/xano-features/metadata-api/instance_api/update_an_existing_workspace) |
