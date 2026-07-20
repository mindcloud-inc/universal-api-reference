# <img src="https://images.mindcloud.co/apps/icons/easy-content_1774985268794.png" alt="EasyContent logo" width="28" height="28"> EasyContent: Universal API

Content API for EasyContent.io

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyContent/latest
- **Category:** Website & App Building / CMS
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://easycontent.io
- **Vendor API docs:** https://easycontent.io/content-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Key](actions/check-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | GET | Checks an EasyContent API key and returns its project. |
| [Check Zapier Auth](actions/check-zapier-auth.md) | GET | Checks an EasyContent Zapier API key and returns its account. |

### Brief

| Action | Method | Description |
| --- | --- | --- |
| [Get Brief](actions/get-brief.md) | GET | Retrieves a brief from EasyContent by ID. |
| [List Briefs](actions/list-briefs.md) | GET | Retrieves briefs from the connected EasyContent project. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from EasyContent by ID. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from the connected EasyContent project. |
| [List Project Categories](actions/list-project-categories.md) | GET | Retrieves categories from a selected EasyContent project. |

### Content Item

| Action | Method | Description |
| --- | --- | --- |
| [Change Content Item Assignees And Due Dates](actions/change-content-item-assignees-and-due-dates.md) | PUT | Updates assignees or due dates for an EasyContent item. |
| [Change Content Item Status](actions/change-content-item-status.md) | PUT | Updates a content item's workflow status in EasyContent. |
| [Create Item](actions/create-item.md) | POST | Creates a new content item in EasyContent. |
| [Get Content Item](actions/get-content-item.md) | GET | Retrieves a content item from EasyContent by ID. |
| [List Content Items](actions/list-content-items.md) | GET | Retrieves content items from the connected EasyContent project. |
| [List Project Content Items](actions/list-project-content-items.md) | GET | Retrieves content items from a selected EasyContent project. |
| [List Template Content Items](actions/list-template-content-items.md) | GET | Retrieves EasyContent items that use a specific template. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects available to the connected EasyContent account. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template structure from EasyContent by ID. |
| [List Project Templates](actions/list-project-templates.md) | GET | Retrieves templates from a selected EasyContent project. |
| [List Templates](actions/list-templates.md) | GET | Retrieves active templates from the connected EasyContent project. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Status Users](actions/list-status-users.md) | GET | Retrieves users assignable to a selected EasyContent workflow status. |

### Workflow Status

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | GET | Retrieves workflow statuses from a selected EasyContent project. |

