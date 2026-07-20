# List Styleguide Variable Collections with Zeplin

Retrieves a list of styleguide variable collections from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/variable_collections`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Variable Collections](https://docs.zeplin.dev/reference/getstyleguidevariablecollections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
