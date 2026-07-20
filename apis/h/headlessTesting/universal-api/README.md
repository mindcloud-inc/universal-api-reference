# <img src="https://images.mindcloud.co/apps/icons/headless-testing-icon_1776092551601.png" alt="Headless Testing logo" width="28" height="28"> Headless Testing: Universal API

TestingBot API integration for managing testing resources over the documented REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/headlessTesting/latest
- **Actions:** 59
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://headlesstesting.com
- **Vendor API docs:** https://testingbot.com/support/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (59)

### Available Device

| Action | Method | Description |
| --- | --- | --- |
| [List Available Devices](actions/list-available-devices.md) | GET | Retrieves available devices from Headless Testing. |

### Browser

| Action | Method | Description |
| --- | --- | --- |
| [List Browsers](actions/list-browsers.md) | GET | Retrieves browsers from Headless Testing. |

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Delete Build](actions/delete-build.md) | DELETE | Deletes a build from Headless Testing. |
| [Get Build](actions/get-build.md) | GET | Retrieves a build from Headless Testing. |
| [List Builds](actions/list-builds.md) | GET | Retrieves builds from Headless Testing. |

### Codeless Suite

| Action | Method | Description |
| --- | --- | --- |
| [Create Codeless Suite](actions/create-codeless-suite.md) | POST | Creates a codeless suite in Headless Testing. |
| [Delete Codeless Suite](actions/delete-codeless-suite.md) | DELETE | Deletes a codeless suite from Headless Testing. |
| [Get Codeless Suite](actions/get-codeless-suite.md) | GET | Retrieves a codeless suite from Headless Testing. |
| [List Codeless Suites](actions/list-codeless-suites.md) | GET | Retrieves codeless suites from Headless Testing. |

### Codeless Suite Browser

| Action | Method | Description |
| --- | --- | --- |
| [Get Suite Browsers](actions/get-suite-browsers.md) | GET | Retrieves browser assignments for a codeless suite from Headless Testing. |

### Codeless Suite Browser Update

| Action | Method | Description |
| --- | --- | --- |
| [Update Suite Browsers](actions/update-suite-browsers.md) | PUT | Updates browser assignments for a codeless suite in Headless Testing. |

### Codeless Suite Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Codeless Suite](actions/run-codeless-suite.md) | POST | Runs a codeless suite in Headless Testing. |

### Codeless Suite Test

| Action | Method | Description |
| --- | --- | --- |
| [List Suite Tests](actions/list-suite-tests.md) | GET | Retrieves tests in a codeless suite from Headless Testing. |
| [Remove Test From Suite](actions/remove-test-from-suite.md) | DELETE | Removes a test from a codeless suite in Headless Testing. |

### Codeless Suite Test Add

| Action | Method | Description |
| --- | --- | --- |
| [Add Tests To Suite](actions/add-tests-to-suite.md) | POST | Adds tests to a codeless suite in Headless Testing. |

### Codeless Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Codeless Test](actions/create-codeless-test.md) | POST | Creates a codeless test in Headless Testing. |
| [Delete Codeless Test](actions/delete-codeless-test.md) | DELETE | Deletes a codeless test from Headless Testing. |
| [Get Codeless Test](actions/get-codeless-test.md) | GET | Retrieves a codeless test from Headless Testing. |
| [List Codeless Tests](actions/list-codeless-tests.md) | GET | Retrieves codeless tests from Headless Testing. |
| [Update Codeless Test](actions/update-codeless-test.md) | PUT | Updates a codeless test in Headless Testing. |

### Codeless Test Alert

| Action | Method | Description |
| --- | --- | --- |
| [Create Codeless Test Alert](actions/create-codeless-test-alert.md) | POST | Creates a codeless test alert in Headless Testing. |
| [Update Codeless Test Alert](actions/update-codeless-test-alert.md) | PUT | Updates a codeless test alert in Headless Testing. |

### Codeless Test Browser

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Browsers](actions/get-test-browsers.md) | GET | Retrieves browser assignments for a codeless test from Headless Testing. |

### Codeless Test Browser Update

| Action | Method | Description |
| --- | --- | --- |
| [Update Test Browsers](actions/update-test-browsers.md) | PUT | Updates browser assignments for a codeless test in Headless Testing. |

### Codeless Test Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Codeless Test Report](actions/create-codeless-test-report.md) | POST | Creates a codeless test report in Headless Testing. |
| [Update Codeless Test Report](actions/update-codeless-test-report.md) | PUT | Updates a codeless test report in Headless Testing. |

### Codeless Test Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Codeless Test](actions/run-codeless-test.md) | POST | Runs a codeless test in Headless Testing. |

### Codeless Test Run Batch

| Action | Method | Description |
| --- | --- | --- |
| [Run All Codeless Tests](actions/run-all-codeless-tests.md) | POST | Runs all codeless tests in Headless Testing. |

### Codeless Test Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Schedule Codeless Test](actions/schedule-codeless-test.md) | POST | Schedules a codeless test in Headless Testing. |

### Codeless Test Step

| Action | Method | Description |
| --- | --- | --- |
| [List Test Steps](actions/list-test-steps.md) | GET | Retrieves steps for a codeless test from Headless Testing. |

### Codeless Test Step Update

| Action | Method | Description |
| --- | --- | --- |
| [Update Test Steps](actions/update-test-steps.md) | PUT | Updates steps for a codeless test in Headless Testing. |

### Codeless Test Stop

| Action | Method | Description |
| --- | --- | --- |
| [Stop Running Codeless Test](actions/stop-running-codeless-test.md) | PUT | Stops a running codeless test in Headless Testing. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get Device](actions/get-device.md) | GET | Retrieves a device from Headless Testing. |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from Headless Testing. |

### Ip Range

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Ranges](actions/get-ip-ranges.md) | GET | Retrieves IP ranges from Headless Testing. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Job](actions/get-test-job.md) | GET | Retrieves a test job from Headless Testing. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Screenshot](actions/create-screenshot.md) | POST | Creates a screenshot job in Headless Testing. |
| [Get Screenshot](actions/get-screenshot.md) | GET | Retrieves a screenshot job from Headless Testing. |
| [List Screenshots](actions/list-screenshots.md) | GET | Retrieves screenshot jobs from Headless Testing. |

### Storage File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Storage File](actions/delete-storage-file.md) | DELETE | Deletes a storage file from Headless Testing. |
| [Get Storage File](actions/get-storage-file.md) | GET | Retrieves a storage file from Headless Testing. |
| [List Storage Files](actions/list-storage-files.md) | GET | Retrieves storage files from Headless Testing. |
| [Update Storage File](actions/update-storage-file.md) | PUT | Updates a storage file in Headless Testing. |
| [Upload Storage File](actions/upload-storage-file.md) | POST | Uploads a storage file to Headless Testing. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Info](actions/get-team-info.md) | GET | Retrieves team information from Headless Testing. |

### Team User

| Action | Method | Description |
| --- | --- | --- |
| [Create Team User](actions/create-team-user.md) | POST | Creates a team user in Headless Testing. |
| [Get Team User](actions/get-team-user.md) | GET | Retrieves a team user from Headless Testing. |
| [List Team Users](actions/list-team-users.md) | GET | Retrieves team users from Headless Testing. |
| [Update Team User](actions/update-team-user.md) | PUT | Updates a team user in Headless Testing. |

### Team User Credential Reset

| Action | Method | Description |
| --- | --- | --- |
| [Reset Team User Credentials](actions/reset-team-user-credentials.md) | PUT | Resets a team user's credentials in Headless Testing. |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [Delete Test](actions/delete-test.md) | DELETE | Deletes a test from Headless Testing. |
| [Get Test](actions/get-test.md) | GET | Retrieves a test from Headless Testing. |
| [List Tests](actions/list-tests.md) | GET | Retrieves tests from Headless Testing. |
| [Update Test](actions/update-test.md) | PUT | Updates a test in Headless Testing. |

### Test Stop Result

| Action | Method | Description |
| --- | --- | --- |
| [Stop Test](actions/stop-test.md) | PUT | Stops a running test in Headless Testing. |

### Tunnel

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tunnel](actions/delete-tunnel.md) | DELETE | Deletes a tunnel from Headless Testing. |
| [List Tunnels](actions/list-tunnels.md) | GET | Retrieves tunnels from Headless Testing. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user information from Headless Testing. |
| [Update User Info](actions/update-user-info.md) | PUT | Updates user information in Headless Testing. |

