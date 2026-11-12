# List Quotes with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [List Quotes](https://developer.getjobber.com/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Select the Jobber quote fields to return. |
| `createdAfter` | body | `date` | no | Only return quotes created after this timestamp (ISO 8601). Maps to filter.createdAt.after on the Jobber quotes query. |
