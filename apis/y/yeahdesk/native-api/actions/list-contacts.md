# List contacts with Yeahdesk

Retrieves contacts from Yeahdesk using optional search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/person/read`
- **Base URL:** `https://app.yeahdesk.ru/api`
- **Official documentation:** [List contacts](https://help.yeahdesk.ru/docs/for-developers/http-api/contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Return the contact with the specified ID. |
| `search` | query | `string` | no | Search contact names and contact values using a regular expression. |
| `type` | query | `string` | no | Filter by contact data type. |
| `service` | query | `string` | no | Filter by service name. |
| `needExistingRecords` | query | `boolean` | no | When set, return only non-deleted contacts. |
