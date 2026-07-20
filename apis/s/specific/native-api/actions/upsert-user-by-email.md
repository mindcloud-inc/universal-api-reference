# Upsert User By Email with Specific

Creates or updates a user in Specific by email.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Upsert User By Email](https://public-api.specific.app/docs/mutations/createOrUpdateUser)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.email` | body | `string` | yes |
| `variables.id` | body | `string` | no |
| `variables.name` | body | `string` | yes |
