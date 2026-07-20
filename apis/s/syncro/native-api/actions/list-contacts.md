# List Contacts with Syncro

Retrieves a list of contacts from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Contacts](https://api-docs.syncromsp.com/#/Contact/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `number` | no | Any contacts attached to a Customer ID. |
| `page` | query | `number` | no | Returns the provided page of results. |
