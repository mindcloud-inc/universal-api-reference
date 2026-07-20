# List Generated Objects with API Template

Retrieves generated objects from API Template.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/list-objects`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [List Generated Objects](https://apitemplate.io/apiv2/#tag/API-Integration/operation/list-objects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | query | `string` | no | Filter generated objects by template ID. |
| `transaction_ref` | query | `string` | no | Filter objects by transaction reference. |
| `transaction_type` | query | `string` | no | Filter objects by transaction type. |
