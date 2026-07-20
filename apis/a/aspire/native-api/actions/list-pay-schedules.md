# List Pay Schedules with Aspire

Retrieves takeoff groups from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `PaySchedules`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Pay Schedules](https://guide.youraspire.com/apidocs/pay-schedules-1)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
