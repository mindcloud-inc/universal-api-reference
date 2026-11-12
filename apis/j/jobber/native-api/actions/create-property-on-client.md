# Create Property on Client with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [Create Property on Client](https://developer.getjobber.com/docs/using_jobbers_api/api_queries_and_mutations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `string` | yes | Jobber client ID that will own the property. |
| `street1` | body | `string` | no | First street line. |
| `street2` | body | `string` | no | Second street line. |
| `city` | body | `string` | no | Property city. |
| `province` | body | `string` | no | Property province or state. |
| `postalCode` | body | `string` | no | Property postal code. |
| `country` | body | `string` | no | Property country. |
