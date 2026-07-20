# Upsert User By ID with Specific

Creates or updates a user in Specific by ID.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Upsert User By ID](https://public-api.specific.app/docs/mutations/createOrUpdateUser)

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
