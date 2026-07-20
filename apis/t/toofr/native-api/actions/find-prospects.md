# Find Prospects with Toofr

Finds prospects in Toofr by title or company.

## Endpoint

- **Method:** `GET`
- **Path:** `/prospect`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Find Prospects](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | query | `string` | yes | Company name to search prospects for. |
| `count` | query | `number` | yes | Number of prospects to return. |
| `page` | query | `number` | no | Optional provider page number. |
| `title` | query | `string` | yes | Prospect job title to search for. |
| `tld` | query | `string` | no | Optional company top-level domain filter. |
