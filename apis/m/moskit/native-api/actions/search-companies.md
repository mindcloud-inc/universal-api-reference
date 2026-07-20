# Search Companies with Moskit

Finds companies in Moskit by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `companies/search`
- **Base URL:** `https://api.ms.prod.moskit.services/v2`
- **Official documentation:** [Search Companies](https://moskit.stoplight.io/docs/api-v2/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditions[]` | body | `array<object>` | yes | Array of search conditions. Each item needs a field, expression, and optional values array. |
| `conditions[].expression` | body | `string` | yes | Search expression such as like, one_of, null, or not_null. |
| `conditions[].field` | body | `string` | yes | Search field key returned by GET /companies/search. |
| `conditions[].values[]` | body | `array<string>` | no | Optional values array for the condition. Leave empty for null or not_null expressions. |
