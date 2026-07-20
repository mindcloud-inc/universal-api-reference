# List Organization Member Styleguides with Zeplin

Retrieves a list of organization member styleguides from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/members/{member_id}/styleguides`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Member Styleguides](https://docs.zeplin.dev/reference/getorganizationmemberstyleguides)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `member_id` | path | `string` | yes | Member id |
