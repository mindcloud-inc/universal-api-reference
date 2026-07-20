# Get Company By ID with Specific

Retrieves a company from Specific by ID.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Get Company By ID](https://public-api.specific.app/docs/queries/companies)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.id` | body | `string` | yes |
