# List Styleguide Pages with Zeplin

Retrieves a list of styleguide pages from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/pages`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Pages](https://docs.zeplin.dev/reference/getstyleguidepages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
