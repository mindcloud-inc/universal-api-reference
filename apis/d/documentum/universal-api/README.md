# <img src="https://images.mindcloud.co/apps/icons/documentum_1776778195107.png" alt="Documentum logo" width="28" height="28"> Documentum: Universal API

Manage enterprise content, repositories, documents, folders, workflows, permissions, lifecycle operations, and compliant content processes in OpenText Documentum Content Management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documentum/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.opentext.com/products/documentum-content-management
- **Vendor API docs:** https://opentext.github.io/d2sv-sdk/23.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Repositories](actions/list-repositories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Export Object Audit](actions/export-object-audit.md) | GET |  |
| [Get Audit Trail Event Source Facets](actions/get-audit-trail-event-source-facets.md) | GET |  |
| [Get Audit Trail Relative Date Facets](actions/get-audit-trail-relative-date-facets.md) | GET |  |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Creation Profile](actions/get-creation-profile.md) | GET |  |
| [Get D2 Type](actions/get-d2-type.md) | GET |  |
| [Get Search Configuration](actions/get-search-configuration.md) | GET |  |
| [List Creation Profiles](actions/list-creation-profiles.md) | GET |  |
| [List D2 Types](actions/list-d2-types.md) | GET |  |
| [List Search Configurations](actions/list-search-configurations.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Apply Lifecycle State](actions/apply-lifecycle-state.md) | PUT |  |
| [Apply Template To Object](actions/apply-template-to-object.md) | PUT |  |
| [Check In Object Version](actions/check-in-object-version.md) | PUT |  |
| [Create D2 Object](actions/create-d2-object.md) | POST |  |
| [Get Native Annotations](actions/get-native-annotations.md) | GET |  |
| [List C2 Print URLs](actions/list-c2-print-urls.md) | GET |  |
| [List C2 View URLs](actions/list-c2-view-urls.md) | GET |  |
| [List Preview URLs](actions/list-preview-urls.md) | GET |  |
| [Run Query Form Search](actions/run-query-form-search.md) | GET |  |
| [Run Quick Search](actions/run-quick-search.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Export Object Locations](actions/export-object-locations.md) | GET |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Update Workflow Task Notes](actions/update-workflow-task-notes.md) | PUT |  |

### Repositories

| Action | Method | Description |
| --- | --- | --- |
| [List Repositories](actions/list-repositories.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Report Tasks](actions/get-workflow-report-tasks.md) | GET |  |
| [Get Workflow Task Status](actions/get-workflow-task-status.md) | GET |  |
| [List Workflow Tasks](actions/list-workflow-tasks.md) | GET |  |
| [Update Workflow Task Status](actions/update-workflow-task-status.md) | PUT |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Document Templates](actions/list-document-templates.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Encrypted DM Ticket](actions/get-encrypted-dm-ticket.md) | GET |  |

