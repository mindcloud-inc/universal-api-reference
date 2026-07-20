# <img src="https://images.mindcloud.co/apps/icons/common-ninja_1774904619607.png" alt="Common Ninja logo" width="28" height="28"> Common Ninja: Universal API

Common Ninja is a website-widget platform with APIs for managing widgets, projects, contacts, submissions, and widget analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/commonNinja/latest
- **Category:** Website & App Building / CMS
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.commoninja.com
- **Vendor API docs:** https://developers.commoninja.com/docs/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Details](actions/get-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a project contact from Common Ninja. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves project contacts from Common Ninja. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a project submission from Common Ninja. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves project submissions from Common Ninja. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Common Ninja. |
| [List Projects](actions/list-projects.md) | GET | Retrieves user projects from Common Ninja. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves user details from Common Ninja. |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Create Widget](actions/create-widget.md) | POST | Creates a widget in Common Ninja. |
| [Delete Widget](actions/delete-widget.md) | DELETE | Deletes a widget from Common Ninja. |
| [Get Widget](actions/get-widget.md) | GET | Retrieves a widget from Common Ninja. |
| [Get Widget Editor URL](actions/get-widget-editor-url.md) | GET | Retrieves a widget editor URL from Common Ninja. |
| [Get Widget Embed Code](actions/get-widget-embed-code.md) | GET | Retrieves a widget embed code from Common Ninja. |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves user widgets from Common Ninja. |
| [Update Widget](actions/update-widget.md) | PUT | Updates a widget in Common Ninja. |

### Widget Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget Analytics](actions/get-widget-analytics.md) | GET | Retrieves widget analytics from Common Ninja. |

### Widget Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget Type](actions/get-widget-type.md) | GET | Retrieves a widget type from Common Ninja. |
| [List Widget Types](actions/list-widget-types.md) | GET | Retrieves widget types from Common Ninja. |

### Widget Type Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget Type Schema](actions/get-widget-type-schema.md) | GET | Retrieves a widget type schema from Common Ninja. |

