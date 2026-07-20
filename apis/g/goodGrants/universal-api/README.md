# <img src="https://images.mindcloud.co/apps/icons/good-grants_1775662460958.png" alt="Good Grants logo" width="28" height="28"> Good Grants: Universal API

Good Grants is grants management software for running grant, award, and scholarship programs. This app wraps the official Good Grants API for working with forms, applications, users, funds, seasons, and related grant-program resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goodGrants/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://goodgrants.com
- **Vendor API docs:** https://apidocs.goodgrants.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodGrants/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get account](actions/get-account.md) | GET | Retrieves account details from Good Grants. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create application](actions/create-application.md) | POST | Creates a new application in Good Grants. |
| [Delete application](actions/delete-application.md) | DELETE | Deletes an existing application from Good Grants. |
| [Get application](actions/get-application.md) | GET | Retrieves an application from Good Grants. |
| [List applications](actions/list-applications.md) | GET | Retrieves applications from Good Grants. |
| [Update application](actions/update-application.md) | PUT | Updates an existing application in Good Grants. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List categories](actions/list-categories.md) | GET | Retrieves categories from Good Grants. |

### Chapter

| Action | Method | Description |
| --- | --- | --- |
| [List chapters](actions/list-chapters.md) | GET | Retrieves chapters from Good Grants. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create field](actions/create-field.md) | POST | Creates a new field in Good Grants. |
| [List fields](actions/list-fields.md) | GET | Retrieves fields from Good Grants. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get form](actions/get-form.md) | GET | Retrieves a form from Good Grants. |
| [List forms](actions/list-forms.md) | GET | Retrieves forms from Good Grants. |

### Grant Status

| Action | Method | Description |
| --- | --- | --- |
| [List grant statuses](actions/list-grant-statuses.md) | GET | Retrieves grant statuses from Good Grants. |

### Season

| Action | Method | Description |
| --- | --- | --- |
| [List seasons](actions/list-seasons.md) | GET | Retrieves seasons from Good Grants. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create user](actions/create-user.md) | POST | Creates a new user in Good Grants. |
| [Delete user](actions/delete-user.md) | DELETE | Deletes an existing user from Good Grants. |
| [Get user](actions/get-user.md) | GET | Retrieves a user from Good Grants by slug or email. |
| [List users](actions/list-users.md) | GET | Retrieves users from Good Grants. |
| [Update user](actions/update-user.md) | PUT | Updates an existing user in Good Grants. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create webhook](actions/create-webhook.md) | POST | Creates a new webhook in Good Grants. |
| [Delete webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Good Grants. |
| [Get webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Good Grants. |
| [List webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Good Grants. |
| [Update webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Good Grants. |

