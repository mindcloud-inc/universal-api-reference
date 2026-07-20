# List API keys with Unkey

Retrieves API keys from Unkey for an API namespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/apis.listKeys`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [List API keys](https://unkey.com/docs/api-reference/apis/list-api-keys)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `apiId` | body | `string` | yes |
