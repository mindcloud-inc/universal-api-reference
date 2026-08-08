# List Content Webhook History with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-content-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [List Content Webhook History](https://integration-docs.xoi.io/guides/content/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.gte` | body | `date` | no |
| `variables.lte` | body | `date` | no |
| `variables.ascending` | body | `boolean` | no |
