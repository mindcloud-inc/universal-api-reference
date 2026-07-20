# List Organization Styleguides with Zeplin

Retrieves a list of organization styleguides from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/styleguides`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Styleguides](https://docs.zeplin.dev/reference/getorganizationstyleguides)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
