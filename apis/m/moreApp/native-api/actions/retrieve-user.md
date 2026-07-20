# Retrieve User with MoreApp

Retrieves a user from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/customers/{{customerId}}/users/{{userId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve User](https://docs.moreapp.com/docs/developer-docs/504d734002123-retrieve-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `userId` | path | `string` | yes | MoreApp user identifier. |
