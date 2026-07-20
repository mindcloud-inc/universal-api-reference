# List Servers with SqlBak

Retrieves servers from SqlBak.

## Endpoint

- **Method:** `GET`
- **Path:** `/servers`
- **Base URL:** `https://sqlbak.com/public-api/v1`
- **Official documentation:** [List Servers](https://sqlbak.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter servers whose name contains this substring. |
| `app_type` | query | `list` | no | Filter servers by installed SqlBak application type. Accepted values: `sqlbak_linux`, `sqlbak_windows`. |
| `status` | query | `list` | no | Filter servers by current connection status. Accepted values: `disconnected`, `offline`, `online`. |
