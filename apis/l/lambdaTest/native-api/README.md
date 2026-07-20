# LambdaTest: Native API Reference

A consolidated summary of LambdaTest's API configuration and 47 documented operations, with links to official documentation.

- **Official docs:** https://www.lambdatest.com/support/api-doc/
- **OpenAPI specification:** https://swagger-api-support.lambdatest.com/openapi.yaml
- **API base URL:** `https://api.lambdatest.com/automation/api/v1`

## Authentication

### Basic Auth

Authenticate to LambdaTest APIs with HTTP Basic auth. Use your LambdaTest username as Username and your LambdaTest access key as Password.

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

[Official authentication documentation](https://www.lambdatest.com/support/docs/hyperexecute-how-to-get-my-username-and-access-key/)

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (47 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Build](actions/delete-build.md) | `DELETE /builds/{build_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Delete File Extension](actions/delete-file-extension.md) | `DELETE /files/extensions/delete` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Delete Pre-Run File](actions/delete-pre-run-file.md) | `DELETE /files/delete` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Delete Session](actions/delete-session.md) | `DELETE /sessions/{session_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Delete Tunnel](actions/delete-tunnel.md) | `DELETE /tunnels/{tunnel_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Delete User File](actions/delete-user-file.md) | `DELETE /user-files/delete` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Download Pre-Run File](actions/download-pre-run-file.md) | `PUT /files/download` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Download Session Full HAR](actions/download-session-full-har.md) | `GET /sessions/{session_id}/log/full-har` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Download Session Full HAR V2](actions/download-session-full-harv2.md) | `GET /sessions/{session_id}/v2/log/full-har` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Download Session Network HAR](actions/download-session-network-har.md) | `GET /sessions/{session_id}/log/network.har` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Download Session Network HAR V2](actions/download-session-network-harv2.md) | `GET /sessions/{session_id}/v2/log/network.har` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Download User File](actions/download-user-file.md) | `PUT /user-files/download` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Auto-Heal Test](actions/get-auto-heal-test.md) | `GET /autoheal/test/{test_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Build](actions/get-build.md) | `GET /builds/{build_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Geolocation IPs](actions/get-geolocation-i-ps.md) | `GET /geoLocation/ips` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Organization Concurrency](actions/get-organization-concurrency.md) | `GET /org/concurrency` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session](actions/get-session.md) | `GET /sessions/{session_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Command Logs](actions/get-session-command-logs.md) | `GET /sessions/{session_id}/log/command` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Command Logs V2](actions/get-session-command-logs-v2.md) | `GET /sessions/{session_id}/v2/log/command` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Console Logs](actions/get-session-console-logs.md) | `GET /sessions/{session_id}/log/console` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Console Logs V2](actions/get-session-console-logs-v2.md) | `GET /sessions/{session_id}/v2/log/console` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Exceptions](actions/get-session-exceptions.md) | `POST /sessions/{session_id}/exceptions` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Network Logs](actions/get-session-network-logs.md) | `GET /sessions/{session_id}/log/network` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Network Logs V2](actions/get-session-network-logs-v2.md) | `GET /sessions/{session_id}/v2/log/network` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Screenshots](actions/get-session-screenshots.md) | `GET /sessions/{session_id}/screenshots` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Selenium Logs](actions/get-session-selenium-logs.md) | `GET /sessions/{session_id}/log/selenium` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Selenium Logs V2](actions/get-session-selenium-logs-v2.md) | `GET /sessions/{session_id}/v2/log/selenium` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Terminal Logs](actions/get-session-terminal-logs.md) | `POST /sessions/{session_id}/terminal-logs` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Session Video](actions/get-session-video.md) | `GET /sessions/{session_id}/video` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Test Exceptions](actions/get-test-exceptions.md) | `POST /tests/{test_id}/exceptions` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Get Test Video](actions/get-test-video.md) | `GET /test/{test_id}/video` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List Builds](actions/list-builds.md) | `GET /builds` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List File Extensions](actions/list-file-extensions.md) | `GET /files/extensions` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List Platforms](actions/list-platforms.md) | `GET /platforms` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List Pre-Run Files](actions/list-pre-run-files.md) | `GET /files` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List Resolutions](actions/list-resolutions.md) | `GET /resolutions` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List Tunnels](actions/list-tunnels.md) | `GET /tunnels` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [List User Files](actions/list-user-files.md) | `GET /user-files` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Stop Build](actions/stop-build.md) | `PUT /build/stop` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Stop Session](actions/stop-session.md) | `PUT /sessions/{session_id}/stop` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Update Build](actions/update-build.md) | `PATCH /builds/{build_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Update Session](actions/update-session.md) | `PATCH /sessions/{session_id}` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Upload File Extension](actions/upload-file-extension.md) | `POST /files/extensions` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Upload Pre-Run File](actions/upload-pre-run-file.md) | `POST /files` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Upload User File](actions/upload-user-file.md) | `POST /user-files` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
| [Validate Pre-Run File](actions/validate-pre-run-file.md) | `POST /files/validate` | [docs](https://swagger-api-support.lambdatest.com/index.html) |
