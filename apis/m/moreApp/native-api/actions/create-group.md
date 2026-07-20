# Create Group with MoreApp

Creates a group in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/customers/{{customerId}}/groups`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Group](https://docs.moreapp.com/docs/developer-docs/9a2a824bacb05-create-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `name` | body | `string` | yes | Group name. |
