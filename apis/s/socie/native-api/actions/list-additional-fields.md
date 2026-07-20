# List Additional Fields with Socie

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/additional_fields`
- **Base URL:** `https://api.socie.nl`
- **Official documentation:** [List Additional Fields](https://resources.socie.nl/docs/api/resource_Additional_Fields.html#resource_Additional_Fields_getAdditionalFields_context_sort_skip_limit_GET)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of additional fields to return. |
| `skip` | query | `number` | no | Number of additional fields to skip before returning results. |
| `sort` | query | `string` | no | Sort fields in Socie format, for example orderNumber:asc. |
