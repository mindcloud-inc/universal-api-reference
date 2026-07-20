# List User Styleguides with Zeplin

Retrieves a list of user styleguides from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/me/styleguides`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List User Styleguides](https://docs.zeplin.dev/reference/getuserstyleguides)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by status |
