# e-Gov: Native API Reference

A consolidated summary of e-Gov's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://data.e-gov.go.jp/data/api_guide
- **API base URL:** `https://data.e-gov.go.jp/data/api/action`

## Authentication

### No Authentication

This API does not require request authentication.

[Official authentication documentation](https://data.e-gov.go.jp/data/api_guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Datasets](actions/autocomplete-datasets.md) | `GET /package_autocomplete` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_autocomplete) |
| [Autocomplete Formats](actions/autocomplete-formats.md) | `GET /format_autocomplete` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=format_autocomplete) |
| [Autocomplete Groups](actions/autocomplete-groups.md) | `GET /group_autocomplete` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_autocomplete) |
| [Autocomplete Organizations](actions/autocomplete-organizations.md) | `GET /organization_autocomplete` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=organization_autocomplete) |
| [Check Site Readability](actions/check-site-readability.md) | `GET /site_read` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=site_read) |
| [Get Action Help](actions/get-action-help.md) | `GET /help_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=help_show) |
| [Get Dataset](actions/get-dataset.md) | `GET /package_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_show) |
| [Get Group](actions/get-group.md) | `GET /group_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_show) |
| [Get Organization](actions/get-organization.md) | `GET /organization_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=organization_show) |
| [Get Resource](actions/get-resource.md) | `GET /resource_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=resource_show) |
| [Get Site Status](actions/get-site-status.md) | `GET /status_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=status_show) |
| [Get Tag Details](actions/get-tag-details.md) | `GET /tag_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=tag_show) |
| [List Dataset Activity](actions/list-dataset-activity.md) | `GET /package_activity_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_activity_list) |
| [List Dataset Names](actions/list-dataset-names.md) | `GET /package_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_list) |
| [List Dataset Relationships](actions/list-dataset-relationships.md) | `GET /package_relationships_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_relationships_list) |
| [List Datasets With Resources](actions/list-datasets-with-resources.md) | `GET /current_package_list_with_resources` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=current_package_list_with_resources) |
| [List Group Activity](actions/list-group-activity.md) | `GET /group_activity_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_activity_list) |
| [List Group Datasets](actions/list-group-datasets.md) | `GET /group_package_show` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_package_show) |
| [List Group Members](actions/list-group-members.md) | `GET /member_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=member_list) |
| [List Groups](actions/list-groups.md) | `GET /group_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_list) |
| [List Licenses](actions/list-licenses.md) | `GET /license_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=license_list) |
| [List Organization Activity](actions/list-organization-activity.md) | `GET /organization_activity_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=organization_activity_list) |
| [List Organizations](actions/list-organizations.md) | `GET /organization_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=organization_list) |
| [List Recently Changed Dataset Activity](actions/list-recently-changed-dataset-activity.md) | `GET /recently_changed_packages_activity_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=recently_changed_packages_activity_list) |
| [List Tag Vocabularies](actions/list-tag-vocabularies.md) | `GET /vocabulary_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=vocabulary_list) |
| [List Tags](actions/list-tags.md) | `GET /tag_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=tag_list) |
| [List User Activity](actions/list-user-activity.md) | `GET /user_activity_list` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=user_activity_list) |
| [Search Datasets](actions/search-datasets.md) | `GET /package_search` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_search) |
| [Search Resources](actions/search-resources.md) | `GET /resource_search` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=resource_search) |
| [Search Tags](actions/search-tags.md) | `GET /tag_search` | [docs](https://data.e-gov.go.jp/data/api/3/action/help_show?name=tag_search) |
