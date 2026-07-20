# List Dashboards with ThingsBoard

Retrieves dashboard info records from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/tenant/dashboards`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Dashboards](https://thingsboard.cloud/swagger-ui/index.html#/dashboard-controller/getTenantDashboards_1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | yes | Maximum number of dashboard records to return in one page. |
| `page` | query | `number` | yes | Zero-based page number. |
