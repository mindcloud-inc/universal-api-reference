# ThingsBoard: Native API Reference

A consolidated summary of ThingsBoard's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://thingsboard.io/docs/paas/reference/rest-api
- **OpenAPI specification:** https://thingsboard.cloud/v3/api-docs
- **API base URL:** `{baseUrl}/api`

## Authentication

### API Key

Connect to a ThingsBoard instance with a base URL and user API key.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Your ThingsBoard instance URL, including protocol, for example https://thingsboard.cloud

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://thingsboard.io/docs/pe/user-guide/security/api-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sortProperty` in the query string. Set the direction separately with `sortOrder`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Alarm](actions/acknowledge-alarm.md) | `POST /alarm/:alarmId/ack` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/ackAlarm) |
| [Clear Alarm](actions/clear-alarm.md) | `POST /alarm/:alarmId/clear` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/clearAlarm) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /asset/:assetId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/asset-controller/deleteAsset) |
| [Delete Device](actions/delete-device.md) | `DELETE /device/:deviceId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/device-controller/deleteDevice) |
| [Find Related Entities](actions/find-related-entities.md) | `POST /relations` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/entity-relation-controller/findByQuery) |
| [Get Alarm](actions/get-alarm.md) | `GET /alarm/:alarmId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/getAlarmById) |
| [Get Asset](actions/get-asset.md) | `GET /asset/:assetId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/asset-controller/getAssetById) |
| [Get Asset Info](actions/get-asset-info.md) | `GET /asset/info/:assetId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/asset-controller/getAssetInfoById) |
| [Get Attributes](actions/get-attributes.md) | `GET /plugins/telemetry/:entityType/:entityId/values/attributes` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/telemetry-controller/getAttributes) |
| [Get Current User](actions/get-current-user.md) | `GET /auth/user` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/auth-controller/getUser) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:customerId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/customer-controller/getCustomerById) |
| [Get Customer Info](actions/get-customer-info.md) | `GET /customer/info/:customerId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/customer-controller/getCustomerInfoById) |
| [Get Dashboard](actions/get-dashboard.md) | `GET /dashboard/:dashboardId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/dashboard-controller/getDashboardById) |
| [Get Device](actions/get-device.md) | `GET /device/:deviceId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/device-controller/getDeviceById) |
| [Get Time Series](actions/get-time-series.md) | `GET /plugins/telemetry/:entityType/:entityId/values/timeseries` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/telemetry-controller/getLatestTimeseries) |
| [List Alarm Types](actions/list-alarm-types.md) | `GET /alarm/types` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/getAlarmTypes) |
| [List Alarms](actions/list-alarms.md) | `GET /alarm/:entityType/:entityId` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/getAlarms) |
| [List Asset Infos](actions/list-asset-infos.md) | `GET /assetInfos/all` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/asset-controller/getAllAssetInfos) |
| [List Customer Infos](actions/list-customer-infos.md) | `GET /customerInfos/all` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/customer-controller/getAllCustomerInfos) |
| [List Dashboards](actions/list-dashboards.md) | `GET /tenant/dashboards` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/dashboard-controller/getTenantDashboards_1) |
| [List Device Infos](actions/list-device-infos.md) | `GET /deviceInfos/all` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/device-controller/getAllDeviceInfos) |
| [List Relation Infos](actions/list-relation-infos.md) | `GET /relations/info` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/entity-relation-controller/findInfoByTo) |
| [Save Asset](actions/save-asset.md) | `POST /asset` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/asset-controller/saveAsset) |
| [Save Customer](actions/save-customer.md) | `POST /customer` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/customer-controller/saveCustomer) |
| [Save Dashboard](actions/save-dashboard.md) | `POST /dashboard` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/dashboard-controller/saveDashboard) |
| [Save Device](actions/save-device.md) | `POST /device` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/device-controller/saveDevice) |
| [Save Relation](actions/save-relation.md) | `POST /relation` | [docs](https://thingsboard.cloud/swagger-ui/index.html#/entity-relation-controller/saveRelation) |
