# List Campaigns with Vouchery.io

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [List Campaigns](https://docs.vouchery.io/reference/getapiv21campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name_cont` | query | `string` | no | Filter by campaign name containing this value. |
| `team_eq` | query | `string` | no | Filter by exact team. |
| `status_eq` | query | `string` | no | Filter by exact status. |
| `template_eq` | query | `string` | no | Filter by exact template. |
| `loyalty_program` | query | `boolean` | no | Filter loyalty program campaigns. |
