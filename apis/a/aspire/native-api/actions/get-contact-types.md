# Get Workers Comps with Aspire

Retrieve a list of information related to workers' compensation.

## Endpoint

- **Method:** `GET`
- **Path:** `WorkersComps`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Get Workers Comps](https://guide.youraspire.com/apidocs/contacttypes-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Use filter to refine the conditions that must be met in the data that is returned. In SQL this would be most similar to the WHERE clause.  Example: You're searching for Contacts but only want to see the active employees. You might use this filter: "(Active eq true) and (ContactTypeName eq Employee)" |
