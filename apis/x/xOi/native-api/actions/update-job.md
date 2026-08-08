# Update Job with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Update Job](https://integration-docs.xoi.io/guides/jobs/#updating-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | XOi job id input. |
| `variables.customerName` | body | `string` | no | XOi customer name input. |
| `variables.jobLocation` | body | `string` | no | XOi job location input. |
| `variables.workOrderNumber` | body | `string` | no | XOi work order number input. |
| `variables.label` | body | `string` | no | XOi label input. |
