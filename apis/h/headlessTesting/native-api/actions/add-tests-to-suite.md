# Add Tests To Suite with Headless Testing

Adds tests to a codeless suite in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/labsuites/:suiteId/tests`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Add Tests To Suite](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suiteId` | path | `string` | yes | The codeless suite identifier. |
| `test_ids` | body | `string` | yes | Comma-separated codeless test IDs to add to the suite. |
