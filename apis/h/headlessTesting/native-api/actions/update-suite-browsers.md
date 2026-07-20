# Update Suite Browsers with Headless Testing

Updates browser assignments for a codeless suite in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/labsuites/:suiteId/browsers`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Update Suite Browsers](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browser_ids` | body | `string` | yes | Comma-separated browser IDs to assign to the codeless suite. |
| `suiteId` | path | `string` | yes | The codeless suite identifier. |
