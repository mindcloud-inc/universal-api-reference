# <img src="https://images.mindcloud.co/apps/icons/favicon-10_1775159455266.png" alt="Cryotos logo" width="28" height="28"> Cryotos: Universal API

Cryotos is a maintenance, asset, and field service operations platform for work requests, work orders, and maintenance teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cryotos/latest
- **Category:** Support / Field Service
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cryotos.com
- **Vendor API docs:** https://www.cryotos.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Authentication Response

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Template Category Counts By Type](actions/get-workflow-template-category-counts-by-type.md) | GET |  |
| [List Workflow Template Categories](actions/list-workflow-template-categories.md) | GET |  |
| [Search Workflow Template Categories](actions/search-workflow-template-categories.md) | GET |  |

### Current Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Organization](actions/get-current-organization.md) | GET |  |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Template](actions/get-email-template.md) | GET |  |
| [List Email Templates](actions/list-email-templates.md) | GET |  |
| [Search Email Templates](actions/search-email-templates.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Aisles](actions/list-aisles.md) | GET |  |
| [List Bin Locations](actions/list-bin-locations.md) | GET |  |
| [List Bins](actions/list-bins.md) | GET |  |
| [List Racks](actions/list-racks.md) | GET |  |
| [List Shelves](actions/list-shelves.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Email Broadcast Schedules](actions/list-email-broadcast-schedules.md) | GET |  |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [List Requests](actions/list-requests.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [List Public Templates](actions/list-public-templates.md) | GET |  |
| [List Template Histories By Workflow ID](actions/list-template-histories-by-workflow-id.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

