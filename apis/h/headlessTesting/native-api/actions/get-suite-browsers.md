# Get Suite Browsers with Headless Testing

Retrieves browser assignments for a codeless suite from Headless Testing.

## Endpoint

- **Method:** `GET`
- **Path:** `/labsuites/:suiteId/browsers`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Get Suite Browsers](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suiteId` | path | `string` | yes | The codeless suite identifier. |
