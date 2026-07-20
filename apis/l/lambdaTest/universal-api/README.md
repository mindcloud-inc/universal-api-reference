# <img src="https://images.mindcloud.co/apps/icons/testmu-ai-logo_1774903249536.jpeg" alt="LambdaTest logo" width="28" height="28"> LambdaTest: Universal API

Manage LambdaTest web automation builds, sessions, tunnels, files, logs, concurrency, supported platforms, resolutions, geolocation IPs, and auto-heal test insights through the official LambdaTest Automation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lambdaTest/latest
- **Actions:** 47
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lambdatest.com
- **Vendor API docs:** https://www.lambdatest.com/support/api-doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Builds](actions/list-builds.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/list-builds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (47)

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Delete Build](actions/delete-build.md) | DELETE | Deletes an existing build from LambdaTest. |
| [Get Build](actions/get-build.md) | GET | Retrieves a build from LambdaTest. |
| [List Builds](actions/list-builds.md) | GET | Retrieves builds from LambdaTest. |
| [Stop Build](actions/stop-build.md) | PUT | Stops a build in LambdaTest. |
| [Update Build](actions/update-build.md) | PUT | Updates an existing build in LambdaTest. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Pre-Run File](actions/delete-pre-run-file.md) | DELETE | Deletes a pre-run file from LambdaTest. |
| [Delete User File](actions/delete-user-file.md) | DELETE | Deletes a user file from LambdaTest. |
| [Download Pre-Run File](actions/download-pre-run-file.md) | GET | Downloads a pre-run file from LambdaTest. |
| [Download User File](actions/download-user-file.md) | GET | Downloads a user file from LambdaTest. |
| [List Pre-Run Files](actions/list-pre-run-files.md) | GET | Retrieves pre-run files from LambdaTest. |
| [List User Files](actions/list-user-files.md) | GET | Retrieves user files from LambdaTest. |
| [Upload Pre-Run File](actions/upload-pre-run-file.md) | POST | Uploads a pre-run file to LambdaTest. |
| [Upload User File](actions/upload-user-file.md) | POST | Uploads a user file to LambdaTest. |
| [Validate Pre-Run File](actions/validate-pre-run-file.md) | GET | Checks whether a pre-run file is approved by LambdaTest. |

### File Extension

| Action | Method | Description |
| --- | --- | --- |
| [Delete File Extension](actions/delete-file-extension.md) | DELETE | Deletes a file extension from LambdaTest. |
| [List File Extensions](actions/list-file-extensions.md) | GET | Retrieves file extensions from LambdaTest. |
| [Upload File Extension](actions/upload-file-extension.md) | POST | Uploads a file extension to LambdaTest. |

### Geolocation

| Action | Method | Description |
| --- | --- | --- |
| [Get Geolocation IPs](actions/get-geolocation-i-ps.md) | GET | Retrieves geolocation IPs from LambdaTest. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Concurrency](actions/get-organization-concurrency.md) | GET | Retrieves organization concurrency from LambdaTest. |

### Platform

| Action | Method | Description |
| --- | --- | --- |
| [List Platforms](actions/list-platforms.md) | GET | Retrieves platforms from LambdaTest. |

### Resolution

| Action | Method | Description |
| --- | --- | --- |
| [List Resolutions](actions/list-resolutions.md) | GET | Retrieves platform resolutions from LambdaTest. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from LambdaTest. |
| [Download Session Full HAR](actions/download-session-full-har.md) | GET | Retrieves a session full HAR file from LambdaTest. |
| [Download Session Full HAR V2](actions/download-session-full-harv2.md) | GET | Retrieves a session full HAR file v2 from LambdaTest. |
| [Download Session Network HAR](actions/download-session-network-har.md) | GET | Retrieves a session network HAR file from LambdaTest. |
| [Download Session Network HAR V2](actions/download-session-network-harv2.md) | GET | Retrieves a session network HAR file v2 from LambdaTest. |
| [Get Auto-Heal Test](actions/get-auto-heal-test.md) | GET | Retrieves auto-healed commands for a test in LambdaTest. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from LambdaTest. |
| [Get Session Command Logs](actions/get-session-command-logs.md) | GET | Retrieves session command logs from LambdaTest. |
| [Get Session Command Logs V2](actions/get-session-command-logs-v2.md) | GET | Retrieves session command logs v2 from LambdaTest. |
| [Get Session Console Logs](actions/get-session-console-logs.md) | GET | Retrieves session console logs from LambdaTest. |
| [Get Session Console Logs V2](actions/get-session-console-logs-v2.md) | GET | Retrieves session console logs v2 from LambdaTest. |
| [Get Session Exceptions](actions/get-session-exceptions.md) | GET |  |
| [Get Session Network Logs](actions/get-session-network-logs.md) | GET | Retrieves session network logs from LambdaTest. |
| [Get Session Network Logs V2](actions/get-session-network-logs-v2.md) | GET | Retrieves session network logs v2 from LambdaTest. |
| [Get Session Screenshots](actions/get-session-screenshots.md) | GET | Retrieves session screenshots from LambdaTest. |
| [Get Session Selenium Logs](actions/get-session-selenium-logs.md) | GET | Retrieves session selenium logs from LambdaTest. |
| [Get Session Selenium Logs V2](actions/get-session-selenium-logs-v2.md) | GET | Retrieves session selenium logs v2 from LambdaTest. |
| [Get Session Terminal Logs](actions/get-session-terminal-logs.md) | GET |  |
| [Get Session Video](actions/get-session-video.md) | GET | Retrieves a session video from LambdaTest. |
| [Get Test Exceptions](actions/get-test-exceptions.md) | GET |  |
| [Get Test Video](actions/get-test-video.md) | GET | Retrieves a test video from LambdaTest. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from LambdaTest. |
| [Stop Session](actions/stop-session.md) | PUT | Stops a session in LambdaTest. |
| [Update Session](actions/update-session.md) | PUT | Updates an existing session in LambdaTest. |

### Tunnel

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tunnel](actions/delete-tunnel.md) | DELETE | Deletes an existing tunnel from LambdaTest. |
| [List Tunnels](actions/list-tunnels.md) | GET | Retrieves tunnels from LambdaTest. |

