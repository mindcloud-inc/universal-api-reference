# List Fields with MailerLite

Retrieves all subscriber fields from MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/fields`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Fields](https://developers.mailerlite.com/docs/fields#list-all-fields)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[keyword]` | query | `string` | no | Returns partial matches for the field name. |
| `filter[type]` | query | `string` | no | Field type to include. |
| `sort` | query | `string` | no | Sort by name or type. Prefix with - for descending. |
