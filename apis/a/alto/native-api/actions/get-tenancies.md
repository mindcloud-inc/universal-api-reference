# Get Tenancies with Alto

Retrieves tenancy records from your Alto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/tenancies`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Tenancies](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include-tenants` | query | `boolean` | no | Whether to include tenant details in tenancy results. |
