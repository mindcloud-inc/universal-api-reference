# Search Opportunity Groups with Zoho CRM

Finds Opportunity Groups in Zoho CRM by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/Opportunity_Groups/search`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Search Opportunity Groups](https://www.zoho.com/crm/developer/docs/api/v8/search-records.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criteria` | query | `string` | no | Use Zoho criteria syntax. To filter by Deal, use the lookup field API name from the custom module, for example `(Deal:equals:1234567890000000001)` when the field API name is `Deal`. Provide one of Criteria, Email, Phone, or Word. |
| `word` | query | `string` | no | Search by a free-text word. Provide one of Criteria, Email, Phone, or Word. |
| `email` | query | `string` | no | Search by an exact email address. Provide one of Criteria, Email, Phone, or Word. |
| `phone` | query | `string` | no | Search by an exact phone number. Provide one of Criteria, Email, Phone, or Word. |
| `fields` | query | `string` | no | Comma-separated API names of fields to include in the response. |
| `converted` | query | `boolean` | no | Whether to include converted records in the result. |
| `approved` | query | `boolean` | no | Whether to restrict the result to approved records. |
