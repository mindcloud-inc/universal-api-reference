# List Applications with Svix

Retrieves applications from Svix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/app`
- **Base URL:** `https://api.us.svix.com`
- **Official documentation:** [List Applications](https://api.svix.com/docs#operation/v1.application.list)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_apps_with_no_endpoints` | query | `boolean` | no | Exclude applications that have no endpoints. |
| `exclude_apps_with_disabled_endpoints` | query | `boolean` | no | Exclude applications that only have disabled endpoints. |
| `exclude_apps_with_svix_play_endpoints` | query | `boolean` | no | Exclude applications that only have Svix Play endpoints. |
| `limit` | query | `number` | no | Maximum number of returned items. |
| `iterator` | query | `string` | no | Iterator returned from a prior invocation. |
| `order` | query | `string` | no | Sorting order for the returned applications. Accepted values: `0`, `1`. |
