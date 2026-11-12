# Get Job with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Get Job](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Encoded Jobber job ID to retrieve. |
| `columns` | body | `string` | no | Select the Jobber job fields to return. |
