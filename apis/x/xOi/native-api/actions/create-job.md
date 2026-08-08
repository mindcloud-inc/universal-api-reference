# Create Job with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Create Job](https://integration-docs.xoi.io/guides/jobs/#creating-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.assigneeId` | body | `string` | yes | XOi assignee id input. |
| `variables.customerName` | body | `string` | yes | XOi customer name input. |
| `variables.jobLocation` | body | `string` | yes | XOi job location input. |
| `variables.workOrderNumber` | body | `string` | yes | XOi work order number input. |
| `variables.label` | body | `string` | no | XOi label input. |
| `variables.externalId` | body | `string` | no | Optional unique job ID from the external system. |
