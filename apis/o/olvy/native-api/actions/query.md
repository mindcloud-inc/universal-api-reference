# Query with Olvy

Makes an authenticated raw API request to Olvy.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.olvy.co/api/v2/graphql`
- **Official documentation:** [Query](https://app.olvy.co/settings/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Raw GraphQL query document to execute against Olvy. |
