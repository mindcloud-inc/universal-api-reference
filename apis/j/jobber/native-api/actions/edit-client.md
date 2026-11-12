# Edit Client with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Edit Client](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | yes | Jobber client ID to update. |
| `customFields` | body | `string` | no | Optional JSON array of Jobber custom field edits. |
