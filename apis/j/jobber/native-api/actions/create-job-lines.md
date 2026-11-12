# Create Job Lines with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Create Job Lines](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | body | `string` | yes | Jobber job ID that will receive the line items. |
| `lineItems` | body | `string` | yes | JSON array of JobCreateLineItemAttributes. |
