# Update User By ID with Specific

Updates a user in Specific by ID.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Update User By ID](https://public-api.specific.app/docs/mutations/updateUser)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.email` | body | `string` | no |
| `variables.id` | body | `string` | yes |
| `variables.name` | body | `string` | yes |
