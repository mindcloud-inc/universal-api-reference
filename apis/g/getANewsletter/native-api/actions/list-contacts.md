# List Contacts with Get a Newsletter

Lists contacts in Get a Newsletter.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/`
- **Base URL:** `https://api.getanewsletter.com/v3`
- **Official documentation:** [List Contacts](https://api.getanewsletter.com/v3/docs/contacts/#get-contacts)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `ordering` | query | `string` | no |
| `search_email` | query | `string` | no |
| `search_name` | query | `string` | no |
| `lists[]` | query | `array<string>` | no |
| `updated_lt` | query | `date` | no |
| `updated_gt` | query | `date` | no |
| `updated_year` | query | `number` | no |
| `updated_month` | query | `number` | no |
| `updated_day` | query | `number` | no |
| `created_lt` | query | `date` | no |
| `created_gt` | query | `date` | no |
| `created_year` | query | `number` | no |
| `created_month` | query | `number` | no |
| `created_day` | query | `number` | no |
