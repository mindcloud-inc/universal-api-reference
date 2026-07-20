# List Users with Five9

Retrieves users from Five9.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.prod.us.five9.net/users/v1/domains/:domainID/users`
- **Base URL:** `https://api.prod.us.five9.net/acl/v1/`
- **Official documentation:** [List Users](https://documentation.five9.com/bundle/admin-console/page/admin-console/users/_ch-users.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `lastName` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `firstName` | body | `string` | no |
| `domainID` | path | `string` | yes |
