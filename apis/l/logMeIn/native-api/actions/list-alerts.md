# List Alerts with LogMeIn

Retrieves a filtered list of alerts from LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve-alerts/v1/alerts/list`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [List Alerts](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pagination.pageSize` | body | `number` | no | Maximum number of alerts to return. GoTo caps a request at 200 alerts. |
| `pagination.continuationToken` | body | `string` | no | Continuation token for the next page of alerts. |
| `filter.isAcknowledged` | body | `boolean` | no | When provided, returns either active or acknowledged alerts. |
| `filter.deviceIds[]` | body | `array<string>` | no | Device IDs to filter alerts by. |
| `filter.ruleTypes[]` | body | `array<string>` | no | Rule types to filter alerts by. |
| `filter.tenantIds[]` | body | `array<string>` | no | Tenant IDs to filter alerts by. |
| `filter.priorities[]` | body | `array<string>` | no | Alert priorities to filter by. |
| `filter.triggeredBefore` | body | `date` | no | Return alerts triggered before this timestamp. |
| `filter.triggeredAfter` | body | `date` | no | Return alerts triggered after this timestamp. |
| `sorting.property` | body | `string` | no | Alert property to sort by. |
| `sorting.order` | body | `string` | no | Sort order for alerts. |
