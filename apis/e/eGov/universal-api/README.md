# <img src="https://images.mindcloud.co/apps/icons/e-gov_1776359681571.png" alt="e-Gov logo" width="28" height="28"> e-Gov: Universal API

Search and inspect public e-Gov dataset metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eGov/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://data.e-gov.go.jp/data
- **Vendor API docs:** https://data.e-gov.go.jp/data/api_guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Autocomplete Datasets](actions/autocomplete-datasets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-datasets?connectionId=$CONNECTION_ID&q=%E4%BA%A4%E9%80%9A" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Action Help

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Help](actions/get-action-help.md) | GET | Retrieves API action help from e-Gov. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Dataset Activity](actions/list-dataset-activity.md) | GET | Retrieves a dataset's activity stream from e-Gov. |
| [List Group Activity](actions/list-group-activity.md) | GET | Retrieves a group's activity stream from e-Gov. |
| [List Organization Activity](actions/list-organization-activity.md) | GET | Retrieves an organization's activity stream from e-Gov. |
| [List Recently Changed Dataset Activity](actions/list-recently-changed-dataset-activity.md) | GET | Retrieves recently changed dataset activity from e-Gov. |
| [List User Activity](actions/list-user-activity.md) | GET | Retrieves user activity from e-Gov. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset and its resources from e-Gov. |
| [List Datasets With Resources](actions/list-datasets-with-resources.md) | GET | Retrieves datasets with resources from e-Gov. |
| [List Group Datasets](actions/list-group-datasets.md) | GET | Retrieves datasets in a group from e-Gov. |
| [Search Datasets](actions/search-datasets.md) | GET | Finds datasets in e-Gov by search criteria. |

### Dataset Name

| Action | Method | Description |
| --- | --- | --- |
| [List Dataset Names](actions/list-dataset-names.md) | GET | Retrieves dataset names from e-Gov. |

### Dataset Relationship

| Action | Method | Description |
| --- | --- | --- |
| [List Dataset Relationships](actions/list-dataset-relationships.md) | GET | Retrieves a dataset's relationships from e-Gov. |

### Dataset Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Datasets](actions/autocomplete-datasets.md) | GET | Finds datasets in e-Gov by partial name. |

### Format

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Formats](actions/autocomplete-formats.md) | GET | Finds resource formats in e-Gov by partial name. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from e-Gov. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from e-Gov. |

### Group Member

| Action | Method | Description |
| --- | --- | --- |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves group members from e-Gov. |

### Group Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Groups](actions/autocomplete-groups.md) | GET | Finds groups in e-Gov by partial name. |

### License

| Action | Method | Description |
| --- | --- | --- |
| [List Licenses](actions/list-licenses.md) | GET | Retrieves dataset licenses from e-Gov. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from e-Gov. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from e-Gov. |

### Organization Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Organizations](actions/autocomplete-organizations.md) | GET | Finds organizations in e-Gov by partial name. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET | Retrieves resource metadata from e-Gov. |
| [Search Resources](actions/search-resources.md) | GET | Finds resources in e-Gov by search criteria. |

### Site Readability

| Action | Method | Description |
| --- | --- | --- |
| [Check Site Readability](actions/check-site-readability.md) | GET | Checks whether the e-Gov site is readable. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Status](actions/get-site-status.md) | GET | Retrieves site status from e-Gov. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag Details](actions/get-tag-details.md) | GET | Retrieves a tag and its datasets from e-Gov. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from e-Gov. |
| [Search Tags](actions/search-tags.md) | GET | Finds tags in e-Gov by name. |

### Vocabulary

| Action | Method | Description |
| --- | --- | --- |
| [List Tag Vocabularies](actions/list-tag-vocabularies.md) | GET | Retrieves tag vocabularies from e-Gov. |

