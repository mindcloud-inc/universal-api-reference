# Retrieve Group with MoreApp

Retrieves a group from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Group](https://docs.moreapp.com/docs/developer-docs/b747d3ac1da61-retrieve-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `groupId` | path | `string` | yes | MoreApp group identifier. |
