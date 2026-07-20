# List Forms with Refiner

Retrieves forms from your Refiner account.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [List Forms](https://refiner.io/docs/api/#get-forms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | query | `string` | no | Choose which forms to return: all, published, drafts, archived, or all_with_archived. |
| `include_config` | query | `boolean` | no | Include the survey configuration and elements. |
| `include_info` | query | `boolean` | no | Include additional form metadata such as counts and dates. |
