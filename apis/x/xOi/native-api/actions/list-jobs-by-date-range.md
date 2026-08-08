# List Jobs by Date Range with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [List Jobs by Date Range](https://integration-docs.xoi.io/schemas/jobs/#listjobsinput)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.dateType` | body | `string` | yes | Accepted values: `0`, `1`. |
| `variables.gte` | body | `date` | no | — |
| `variables.lte` | body | `date` | no | — |
| `variables.ascending` | body | `boolean` | no | — |
