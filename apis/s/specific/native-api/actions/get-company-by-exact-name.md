# Get Company By Exact Name with Specific

Retrieves a company from Specific by exact name.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [Get Company By Exact Name](https://public-api.specific.app/docs/queries/companies)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.name` | body | `string` | yes |
