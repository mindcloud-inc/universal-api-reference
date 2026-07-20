# Create Service with Pinghome

Creates a new service in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/resource-cmd/v1/service`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Service](https://docs.pinghome.io/customer-account-management/team-organization-and-role-setup/create-service/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the service to create. |
| `team_id` | body | `string` | yes | The team id that will own the service. |
