# List Items with Jobber

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.getjobber.com/api`
- **Official documentation:** [List Items](https://developer.getjobber.com/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Select the Jobber product or service fields to return. |
| `ids` | body | `string` | no | One or more Jobber encoded product or service IDs. Maps to products.filter.ids. Send multiple values as a array. |
