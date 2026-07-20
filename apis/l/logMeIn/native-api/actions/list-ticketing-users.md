# List Ticketing Users with LogMeIn

Retrieves available ticketing users from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/goto-resolve-ticketing/v1/users`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [List Ticketing Users](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceId` | query | `string` | no | Optional service identifier. Leave blank to return users from all services. |
| `userType` | query | `string` | no | User type filter. |
| `limit` | query | `number` | no | Number of users to return. |
| `keyword` | query | `string` | no | Filter users by first name, last name, or email. |
