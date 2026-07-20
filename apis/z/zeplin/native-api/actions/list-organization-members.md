# List Organization Members with Zeplin

Retrieves a list of organization members from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/members`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Members](https://docs.zeplin.dev/reference/getorganizationmembers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `handle[]` | query | `array<string>` | no | Filter organization members by email, username or unique identifier of the user ☝️Note that only organization admins (or higher) can filter members using email addresses. Example: `?handle=zozo&handle=5d9caaecb4a3fa9bc9718686&handle=zozo%40zeplin.io` |
