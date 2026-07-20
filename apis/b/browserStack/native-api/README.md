# BrowserStack: Native API Reference

A consolidated summary of BrowserStack's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://www.browserstack.com/docs/automate/api-reference/selenium/introduction
- **API base URL:** `https://api.browserstack.com`

## Authentication

### Basic Authentication

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.browserstack.com/docs/automate/api-reference/selenium/authentication)

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Build](actions/delete-build.md) | `DELETE /automate/builds/:build_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/build#delete-build) |
| [Delete Media File](actions/delete-media-file.md) | `DELETE https://api-cloud.browserstack.com/automate/custom_media/delete/:media_id` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/media#delete-media-file) |
| [Delete Session](actions/delete-session.md) | `DELETE /automate/sessions/:session_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#delete-session) |
| [Get Automate Plan Details](actions/get-automate-plan-details.md) | `GET /automate/plan.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/plan#get-plan-details) |
| [Get Browser List](actions/get-browser-list.md) | `GET /automate/browsers.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/browser#get-browser-list) |
| [Get Project Details](actions/get-project-details.md) | `GET /automate/projects/:project_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/project#get-project-details) |
| [Get Project Status Badge Key](actions/get-project-status-badge-key.md) | `GET /automate/projects/:project_id/badge_key` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/project#get-status-badge) |
| [Get Session Console Logs](actions/get-session-console-logs.md) | `GET /automate/sessions/:session_id/consolelogs` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-console-logs) |
| [Get Session Details](actions/get-session-details.md) | `GET /automate/sessions/:session_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-details) |
| [Get Session Logs](actions/get-session-logs.md) | `GET /automate/sessions/:session_id/logs` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-logs) |
| [Get Session Selenium Logs](actions/get-session-selenium-logs.md) | `GET /automate/sessions/:session_id/seleniumlogs` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-selenium-logs) |
| [List Builds](actions/list-builds.md) | `GET /automate/builds.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/build#get-build-list) |
| [List Projects](actions/list-projects.md) | `GET /automate/projects.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/project#get-project-list) |
| [List Sessions In Build](actions/list-sessions-in-build.md) | `GET /automate/builds/:build_id/sessions.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-list) |
| [List Uploaded Media Files](actions/list-uploaded-media-files.md) | `GET https://api-cloud.browserstack.com/automate/recent_media_files` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/media#list-uploaded-media-files) |
| [Set Session Status](actions/set-session-status.md) | `PUT /automate/sessions/:session_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#set-test-status) |
| [Update Build Details](actions/update-build-details.md) | `PUT /automate/builds/:build_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/build#update-build-details) |
| [Update Project Details](actions/update-project-details.md) | `PUT /automate/projects/:project_id.json` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/project#update-project-details) |
| [Upload Media File](actions/upload-media-file.md) | `POST https://api-cloud.browserstack.com/automate/upload-media` | [docs](https://www.browserstack.com/docs/automate/api-reference/selenium/media#upload-media-file) |
