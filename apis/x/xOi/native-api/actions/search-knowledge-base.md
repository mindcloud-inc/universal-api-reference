# Search Knowledge Base with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-content-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Search Knowledge Base](https://integration-docs.xoi.io/guides/content/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.searchText` | body | `string` | yes | XOi search text input. |
| `variables.makes[]` | body | `array<string>` | no | — |
| `variables.mediaTypes[]` | body | `array<string>` | no | — |
