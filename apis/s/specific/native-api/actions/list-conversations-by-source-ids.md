# List Conversations By Source IDs with Specific

Retrieves conversations from Specific by source IDs.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://public-api.specific.app/graphql`
- **Official documentation:** [List Conversations By Source IDs](https://public-api.specific.app/docs/queries/conversations)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.sources[]` | body | `array<string>` | yes |
