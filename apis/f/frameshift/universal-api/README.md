# <img src="https://images.mindcloud.co/apps/icons/frameshift_1775498010308.png" alt="Frameshift logo" width="28" height="28"> Frameshift: Universal API

Analyze genomic data and manage Mosaic projects, samples, and variants

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/frameshift/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://frameshift.io
- **Vendor API docs:** https://mosaic.frameshift.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Activity Types](actions/list-activity-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-activity-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Project Activities](actions/list-project-activities.md) | GET | Retrieves a list of project activities from Frameshift. |

### Activity Type

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves a list of activity types from Frameshift. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment in a Frameshift conversation. |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Frameshift. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves detailed conversation information from Frameshift. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves a list of conversations from Frameshift. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Frameshift. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Project File](actions/create-project-file.md) | POST | Creates a project file in Frameshift. |
| [Create Sample](actions/create-sample.md) | POST | Creates a new sample in Frameshift. |
| [Create Sample File](actions/create-sample-file.md) | POST | Creates a sample file in Frameshift. |
| [Create Variant Filter](actions/create-variant-filter.md) | POST | Creates a variant filter in Frameshift. |
| [Delete Sample](actions/delete-sample.md) | DELETE | Deletes an existing sample from Frameshift. |
| [Delete Variant Filter](actions/delete-variant-filter.md) | DELETE | Deletes an existing variant filter from Frameshift. |
| [Get Project File URL](actions/get-project-file-url.md) | GET | Retrieves a project file URL from Frameshift. |
| [Get Sample](actions/get-sample.md) | GET | Retrieves detailed sample information from Frameshift. |
| [Get Sample QC Stats](actions/get-sample-qc-stats.md) | GET | Retrieves sample QC statistics from Frameshift. |
| [Get Variant](actions/get-variant.md) | GET | Retrieves detailed variant information from Frameshift. |
| [Get Variant By Position](actions/get-variant-by-position.md) | GET | Retrieves a variant from Frameshift by position. |
| [Get Variant Set](actions/get-variant-set.md) | GET | Retrieves variant set details from Frameshift. |
| [Get Variant Watchlist](actions/get-variant-watchlist.md) | GET | Retrieves the variant watchlist from Frameshift. |
| [Import Samples](actions/import-samples.md) | POST | Imports samples into a Frameshift project. |
| [List All Sample Files](actions/list-all-sample-files.md) | GET | Retrieves all sample files from Frameshift. |
| [List Project Files](actions/list-project-files.md) | GET | Retrieves a list of project files from Frameshift. |
| [List Project Samples](actions/list-project-samples.md) | GET | Retrieves a list of project samples from Frameshift. |
| [List Project Variants](actions/list-project-variants.md) | GET | Retrieves a list of project variants from Frameshift. |
| [List Sample Files](actions/list-sample-files.md) | GET | Retrieves a list of sample files from Frameshift. |
| [List Variant Filters](actions/list-variant-filters.md) | GET | Retrieves a list of variant filters from Frameshift. |
| [List Variant Sets](actions/list-variant-sets.md) | GET | Retrieves a list of variant sets from Frameshift. |
| [Search Variants By Region](actions/search-variants-by-region.md) | GET | Finds variants in Frameshift by genomic region. |
| [Update Sample](actions/update-sample.md) | PUT | Updates an existing sample in Frameshift. |
| [Update Variant Filter](actions/update-variant-filter.md) | PUT | Updates an existing variant filter in Frameshift. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Frameshift. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Frameshift. |
| [Get Project](actions/get-project.md) | GET | Retrieves detailed project information from Frameshift. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Frameshift. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Frameshift. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Frameshift. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves a list of project tasks from Frameshift. |
| [List Task Types](actions/list-task-types.md) | GET | Retrieves a list of task types from Frameshift. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Frameshift. |

