# Search Contacts with Zoho CRM

Finds contact records in Zoho CRM by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/Contacts/search`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Search Contacts](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criteria` | query | `string` | no | Use Zoho criteria syntax. Provide one of Criteria, Email, Phone, or Word. |
| `word` | query | `string` | no | Search by a free-text word. Provide one of Criteria, Email, Phone, or Word. |
| `email` | query | `string` | no | Search by an exact email address. Provide one of Criteria, Email, Phone, or Word. |
| `phone` | query | `string` | no | Search by an exact phone number. Provide one of Criteria, Email, Phone, or Word. |
| `fields` | query | `string` | no | Comma-separated API names of fields to include in the response. |
| `converted` | query | `boolean` | no | Whether to include converted records in the result. |
| `approved` | query | `boolean` | no | Whether to restrict the result to approved records. |
