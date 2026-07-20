# List Users with Vacation Tracker

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.vacationtracker.io/v1`
- **Official documentation:** [List Users](https://vacationtracker.io/developers/api/users/listUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Filter users by status. Defaults to ACTIVE. Accepted values: `ACTIVE`, `DELETED`, `INACTIVE`. |
| `locations` | query | `string` | no | Comma-separated list of location IDs to filter users. Send multiple values as a string separated by `,`. |
| `departments` | query | `string` | no | Comma-separated list of department IDs to filter users. Send multiple values as a string separated by `,`. |
| `labels` | query | `string` | no | Comma-separated list of labels to filter users. Send multiple values as a string separated by `,`. |
| `expand` | query | `list<string>` | no | Related user object to expand. Accepted values: `department`, `holidays`, `location`. |
