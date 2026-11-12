# Create Job with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Create Job](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | body | `string` | yes | Property ID for the new Jobber job. |
| `scheduling` | body | `string` | yes | JSON object with JobSchedulingAttributes. |
| `invoicing` | body | `string` | yes | JSON object with JobInvoicingAttributes. |
| `title` | body | `string` | no | Optional job title. |
| `customFields` | body | `string` | no | Optional JSON array of custom field inputs. |
