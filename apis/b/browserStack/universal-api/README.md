# <img src="https://images.mindcloud.co/apps/icons/favicon-11_1775163404195.png" alt="BrowserStack logo" width="28" height="28"> BrowserStack: Universal API

Run browser automation and inspect plan, browser, build, and session data in BrowserStack Automate.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/browserStack/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.browserstack.com/
- **Vendor API docs:** https://www.browserstack.com/docs/automate/api-reference/selenium/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Automate Plan Details](actions/get-automate-plan-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/get-automate-plan-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Automate Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Automate Plan Details](actions/get-automate-plan-details.md) | GET | Retrieves Automate plan details from BrowserStack. |

### Browser

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser List](actions/get-browser-list.md) | GET | Retrieves available browsers and devices from BrowserStack Automate. |

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Delete Build](actions/delete-build.md) | DELETE | Deletes an existing build from BrowserStack Automate. |
| [List Builds](actions/list-builds.md) | GET | Retrieves build records from BrowserStack Automate. |
| [Update Build Details](actions/update-build-details.md) | PUT | Updates an existing build in BrowserStack Automate. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Media File](actions/delete-media-file.md) | DELETE | Deletes a media file from BrowserStack Automate. |
| [List Uploaded Media Files](actions/list-uploaded-media-files.md) | GET | Retrieves uploaded media files from BrowserStack Automate. |
| [Upload Media File](actions/upload-media-file.md) | POST | Uploads a media file to BrowserStack Automate. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves project details from BrowserStack Automate. |
| [Get Project Status Badge Key](actions/get-project-status-badge-key.md) | GET | Retrieves a project status badge key from BrowserStack. |
| [List Projects](actions/list-projects.md) | GET | Retrieves project records from BrowserStack Automate. |
| [Update Project Details](actions/update-project-details.md) | PUT | Updates an existing project in BrowserStack Automate. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from BrowserStack Automate. |
| [Get Session Console Logs](actions/get-session-console-logs.md) | GET | Retrieves session console logs from BrowserStack Automate. |
| [Get Session Details](actions/get-session-details.md) | GET | Retrieves session details from BrowserStack Automate. |
| [Get Session Logs](actions/get-session-logs.md) | GET | Retrieves session logs from BrowserStack Automate. |
| [Get Session Selenium Logs](actions/get-session-selenium-logs.md) | GET | Retrieves session Selenium logs from BrowserStack Automate. |
| [List Sessions In Build](actions/list-sessions-in-build.md) | GET | Retrieves build session records from BrowserStack Automate. |
| [Set Session Status](actions/set-session-status.md) | PUT | Updates a session status in BrowserStack Automate. |

