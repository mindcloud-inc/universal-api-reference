# List CRM Contacts with WhatsScale

Retrieves CRM contacts from your WhatsScale account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/crm/contacts`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [List CRM Contacts](https://whatsscale.com/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Results per page, default 50. |
| `page` | query | `number` | no | Page number, default 1. |
| `search` | query | `string` | no | Search by name or phone. |
| `tag` | query | `string` | no | Filter by tag. |
