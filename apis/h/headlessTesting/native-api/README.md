# Headless Testing: Native API Reference

A consolidated summary of Headless Testing's API configuration and 59 documented operations, with links to official documentation.

- **Official docs:** https://testingbot.com/support/api
- **OpenAPI specification:** https://testingbot.com/support/api
- **API base URL:** `https://api.testingbot.com/v1`

## Authentication

### TestingBot Basic Auth

HTTP Basic Auth using the TestingBot API key as username and API secret as password.

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

[Official authentication documentation](https://testingbot.com/support/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (59 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tests To Suite](actions/add-tests-to-suite.md) | `POST /labsuites/:suiteId/tests` | [docs](https://testingbot.com/support/api) |
| [Create Codeless Suite](actions/create-codeless-suite.md) | `POST /labsuites` | [docs](https://testingbot.com/support/api) |
| [Create Codeless Test](actions/create-codeless-test.md) | `POST /lab` | [docs](https://testingbot.com/support/api) |
| [Create Codeless Test Alert](actions/create-codeless-test-alert.md) | `POST /lab/:id/alert` | [docs](https://testingbot.com/support/api) |
| [Create Codeless Test Report](actions/create-codeless-test-report.md) | `POST /lab/:id/report` | [docs](https://testingbot.com/support/api) |
| [Create Screenshot](actions/create-screenshot.md) | `POST /screenshots` | [docs](https://testingbot.com/support/api) |
| [Create Team User](actions/create-team-user.md) | `POST /team-management/users` | [docs](https://testingbot.com/support/api) |
| [Delete Build](actions/delete-build.md) | `DELETE /builds/:buildId` | [docs](https://testingbot.com/support/api) |
| [Delete Codeless Suite](actions/delete-codeless-suite.md) | `DELETE /labsuites/:suiteId` | [docs](https://testingbot.com/support/api) |
| [Delete Codeless Test](actions/delete-codeless-test.md) | `DELETE /lab/:id` | [docs](https://testingbot.com/support/api) |
| [Delete Storage File](actions/delete-storage-file.md) | `DELETE /storage/:app_url` | [docs](https://testingbot.com/support/api) |
| [Delete Test](actions/delete-test.md) | `DELETE /tests/:webdriver_session_id` | [docs](https://testingbot.com/support/api) |
| [Delete Tunnel](actions/delete-tunnel.md) | `DELETE /tunnel/:id` | [docs](https://testingbot.com/support/api) |
| [Get Build](actions/get-build.md) | `GET /builds/:buildId` | [docs](https://testingbot.com/support/api) |
| [Get Codeless Suite](actions/get-codeless-suite.md) | `GET /labsuites/:suiteId` | [docs](https://testingbot.com/support/api) |
| [Get Codeless Test](actions/get-codeless-test.md) | `GET /lab/:id` | [docs](https://testingbot.com/support/api) |
| [Get Device](actions/get-device.md) | `GET /devices/:id` | [docs](https://testingbot.com/support/api) |
| [Get IP Ranges](actions/get-ip-ranges.md) | `GET /configuration/ip-ranges` | [docs](https://testingbot.com/support/api) |
| [Get Screenshot](actions/get-screenshot.md) | `GET /screenshots/:id` | [docs](https://testingbot.com/support/api) |
| [Get Storage File](actions/get-storage-file.md) | `GET /storage/:app_url` | [docs](https://testingbot.com/support/api) |
| [Get Suite Browsers](actions/get-suite-browsers.md) | `GET /labsuites/:suiteId/browsers` | [docs](https://testingbot.com/support/api) |
| [Get Team Info](actions/get-team-info.md) | `GET /team-management` | [docs](https://testingbot.com/support/api) |
| [Get Team User](actions/get-team-user.md) | `GET /team-management/users/:id` | [docs](https://testingbot.com/support/api) |
| [Get Test](actions/get-test.md) | `GET /tests/:webdriver_session_id` | [docs](https://testingbot.com/support/api) |
| [Get Test Browsers](actions/get-test-browsers.md) | `GET /lab/:id/browsers` | [docs](https://testingbot.com/support/api) |
| [Get Test Job](actions/get-test-job.md) | `GET /jobs/:jobId` | [docs](https://testingbot.com/support/api) |
| [Get User Info](actions/get-user-info.md) | `GET /user` | [docs](https://testingbot.com/support/api) |
| [List Available Devices](actions/list-available-devices.md) | `GET /devices/available` | [docs](https://testingbot.com/support/api) |
| [List Browsers](actions/list-browsers.md) | `GET /browsers` | [docs](https://testingbot.com/support/api) |
| [List Builds](actions/list-builds.md) | `GET /builds` | [docs](https://testingbot.com/support/api) |
| [List Codeless Suites](actions/list-codeless-suites.md) | `GET /labsuites` | [docs](https://testingbot.com/support/api) |
| [List Codeless Tests](actions/list-codeless-tests.md) | `GET /lab` | [docs](https://testingbot.com/support/api) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://testingbot.com/support/api) |
| [List Screenshots](actions/list-screenshots.md) | `GET /screenshots` | [docs](https://testingbot.com/support/api) |
| [List Storage Files](actions/list-storage-files.md) | `GET /storage` | [docs](https://testingbot.com/support/api) |
| [List Suite Tests](actions/list-suite-tests.md) | `GET /labsuites/:suiteId/tests` | [docs](https://testingbot.com/support/api) |
| [List Team Users](actions/list-team-users.md) | `GET /team-management/users` | [docs](https://testingbot.com/support/api) |
| [List Test Steps](actions/list-test-steps.md) | `GET /lab/:id/steps` | [docs](https://testingbot.com/support/api) |
| [List Tests](actions/list-tests.md) | `GET /tests` | [docs](https://testingbot.com/support/api) |
| [List Tunnels](actions/list-tunnels.md) | `GET /tunnel/list` | [docs](https://testingbot.com/support/api) |
| [Remove Test From Suite](actions/remove-test-from-suite.md) | `DELETE /labsuites/:suiteId/tests/:testId` | [docs](https://testingbot.com/support/api) |
| [Reset Team User Credentials](actions/reset-team-user-credentials.md) | `PUT /team-management/users/:id/reset-keys` | [docs](https://testingbot.com/support/api) |
| [Run All Codeless Tests](actions/run-all-codeless-tests.md) | `POST /lab/trigger_all` | [docs](https://testingbot.com/support/api) |
| [Run Codeless Suite](actions/run-codeless-suite.md) | `POST /labsuites/:suiteId/trigger` | [docs](https://testingbot.com/support/api) |
| [Run Codeless Test](actions/run-codeless-test.md) | `POST /lab/:id/trigger` | [docs](https://testingbot.com/support/api) |
| [Schedule Codeless Test](actions/schedule-codeless-test.md) | `POST /lab/:id/schedule` | [docs](https://testingbot.com/support/api) |
| [Stop Running Codeless Test](actions/stop-running-codeless-test.md) | `PUT /lab/:id/stop` | [docs](https://testingbot.com/support/api) |
| [Stop Test](actions/stop-test.md) | `PUT /tests/:session_id/stop` | [docs](https://testingbot.com/support/api) |
| [Update Codeless Test](actions/update-codeless-test.md) | `PUT /lab/:id` | [docs](https://testingbot.com/support/api) |
| [Update Codeless Test Alert](actions/update-codeless-test-alert.md) | `PUT /lab/:id/alert` | [docs](https://testingbot.com/support/api) |
| [Update Codeless Test Report](actions/update-codeless-test-report.md) | `PUT /lab/:id/report` | [docs](https://testingbot.com/support/api) |
| [Update Storage File](actions/update-storage-file.md) | `POST /storage/:app_url` | [docs](https://testingbot.com/support/api) |
| [Update Suite Browsers](actions/update-suite-browsers.md) | `POST /labsuites/:suiteId/browsers` | [docs](https://testingbot.com/support/api) |
| [Update Team User](actions/update-team-user.md) | `PUT /team-management/users/:id` | [docs](https://testingbot.com/support/api) |
| [Update Test](actions/update-test.md) | `PUT /tests/:webdriver_session_id` | [docs](https://testingbot.com/support/api) |
| [Update Test Browsers](actions/update-test-browsers.md) | `POST /lab/:id/browsers` | [docs](https://testingbot.com/support/api) |
| [Update Test Steps](actions/update-test-steps.md) | `POST /lab/:id/steps` | [docs](https://testingbot.com/support/api) |
| [Update User Info](actions/update-user-info.md) | `PUT /user` | [docs](https://testingbot.com/support/api) |
| [Upload Storage File](actions/upload-storage-file.md) | `POST /storage` | [docs](https://testingbot.com/support/api) |
