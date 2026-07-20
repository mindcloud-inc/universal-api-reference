# Create Company with Specific

Creates a company in Specific.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Create Company](https://public-api.specific.app/docs/mutations/createCompany)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.attributes` | body | `object` | no |
| `variables.id` | body | `string` | no |
| `variables.name` | body | `string` | yes |
