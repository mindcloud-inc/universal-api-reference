# Get Contacts with AXL

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/lead/table`
- **Base URL:** `https://app.axl.tech/api/v1`
- **Official documentation:** [Get Contacts](https://app.axl.tech/api/public)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | body | `object` | no |
| `fields` | body | `string` | no |
| `filter.skip` | body | `number` | no |
| `filter.take` | body | `number` | no |
