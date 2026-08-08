# List Jobs by Work Order with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [List Jobs by Work Order](https://integration-docs.xoi.io/guides/jobs/#getting-a-list-of-jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.workOrderNumber` | body | `string` | yes | XOi work order number input. |
