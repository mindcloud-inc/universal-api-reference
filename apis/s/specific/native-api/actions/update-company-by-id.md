# Update Company By ID with Specific

Updates a company in Specific by ID.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Update Company By ID](https://public-api.specific.app/docs/mutations/updateCompany)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.id` | body | `string` | yes |
| `variables.name` | body | `string` | yes |
