# List Contacts with Avaza

Retrieves contacts from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Contact`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Contacts](https://api.avaza.com/#!/Contact/Contact_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no |
| `CompanyIDFK` | query | `number` | no |
