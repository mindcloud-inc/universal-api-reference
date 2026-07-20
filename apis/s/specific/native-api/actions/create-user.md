# Create User with Specific

Creates a user in Specific.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Create User](https://public-api.specific.app/docs/mutations/createUser)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.email` | body | `string` | no |
| `variables.id` | body | `string` | no |
| `variables.name` | body | `string` | yes |
