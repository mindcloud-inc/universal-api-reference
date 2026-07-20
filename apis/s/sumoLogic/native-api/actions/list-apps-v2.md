# List Apps V2 with Sumo Logic

Retrieves apps from the Sumo Logic App Catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/apps`
- **Base URL:** `https://api.sumologic.com/api`
- **Official documentation:** [List Apps V2](https://api.sumologic.com/docs/#/appManagementV2/listAppsV2)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Name of the app. |
| `author` | query | `string` | no | Author of the app. |
