# Remove Test From Suite with Headless Testing

Removes a test from a codeless suite in Headless Testing.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/labsuites/:suiteId/tests/:testId`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Remove Test From Suite](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suiteId` | path | `string` | yes | The codeless suite identifier. |
| `testId` | path | `string` | yes | The codeless test identifier in the suite. |
