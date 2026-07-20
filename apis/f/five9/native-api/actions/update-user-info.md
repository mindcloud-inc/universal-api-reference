# Update User with Five9

Updates an existing user in Five9.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.prod.us.five9.net/users/v1/domains/:domainID/users/:userUID`
- **Base URL:** `https://api.prod.us.five9.net/acl/v1/`
- **Official documentation:** [Update User](https://documentation.five9.com/bundle/admin-console/page/admin-console/users/_ch-users.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userUID` | path | `string` | yes |
| `domainID` | path | `string` | yes |
