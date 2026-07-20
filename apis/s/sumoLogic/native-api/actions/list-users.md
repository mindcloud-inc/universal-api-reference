# List Users with Sumo Logic

Retrieves users from your Sumo Logic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users`
- **Base URL:** `https://api.sumologic.com/api`
- **Official documentation:** [List Users](https://api.sumologic.com/docs/#/userManagement/listUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Find a user with the given email address. |
| `includeServiceAccounts` | query | `boolean` | no | Include service accounts while listing users within the organization. |
