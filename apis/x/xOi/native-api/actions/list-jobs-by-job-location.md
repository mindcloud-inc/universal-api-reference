# List Jobs by Job Location with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [List Jobs by Job Location](https://integration-docs.xoi.io/guides/jobs/#getting-a-list-of-jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.jobLocation` | body | `string` | yes | XOi job location input. |
