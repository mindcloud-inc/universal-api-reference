# Poodll: Native API Reference

A consolidated summary of Poodll's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://support.poodll.com/support/solutions/19000105053
- **API base URL:** `{baseUrl}/webservice/rest/server.php`

## Authentication

### Poodll Trigger API Key / Web Token

Connect with your Moodle or Poodll NET site URL and a Poodll Trigger web token.

### Credentials

- **API Key:** `apiKey` · required
- **Site Base URL:** `baseUrl` · required · Base URL of your Moodle or Poodll NET site, for example https://school.example.com

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.poodll.com/support/solutions/articles/19000141629-poodll-trigger-api-key-web-token)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cohort Members](actions/add-cohort-members.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Add Group Members](actions/add-group-members.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/group/externallib.php) |
| [Create Users](actions/create-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php) |
| [Delete Users](actions/delete-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php) |
| [Deregister Webhook](actions/deregister-webhook.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Enrol Users](actions/enrol-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/enrol/manual/externallib.php) |
| [Get Course Groups](actions/get-course-groups.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/group/externallib.php) |
| [Get Courses](actions/get-courses.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/course/externallib.php) |
| [Get Courses By Field](actions/get-courses-by-field.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/course/externallib.php) |
| [Get Custom Action Details](actions/get-custom-action-details.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Get Custom Actions](actions/get-custom-actions.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Get Enrolled Users](actions/get-enrolled-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/enrol/externallib.php) |
| [Get Site Info](actions/get-site-info.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/webservice/externallib.php) |
| [Get Users By Field](actions/get-users-by-field.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php) |
| [Register Webhook](actions/register-webhook.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Remove Cohort Members](actions/remove-cohort-members.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Remove Group Members](actions/remove-group-members.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/group/externallib.php) |
| [Sample Webhook](actions/sample-webhook.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php) |
| [Search Users](actions/search-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php) |
| [Unenrol Users](actions/unenrol-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/enrol/manual/externallib.php) |
| [Update Users](actions/update-users.md) | `POST {{credentials.baseUrl}}/webservice/rest/server.php` | [docs](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php) |
