# List Jobs with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [List Jobs](https://developer.getjobber.com/docs/api-reference/queries/jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Select the Jobber job fields to return. |
| `createdAfter` | body | `date` | no | Only return jobs created after this timestamp (ISO 8601). Maps to filter.createdAt.after on the Jobber jobs query. |
| `createdBefore` | body | `date` | no | Only return jobs created before this timestamp (ISO 8601). Maps to filter.createdAt.before on the Jobber jobs query. |
| `searchTerm` | body | `string` | no | Only return jobs matching this Jobber search term. |
