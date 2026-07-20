# Create Enrichment with BetterContact

Creates an asynchronous BetterContact contact enrichment request.

## Endpoint

- **Method:** `POST`
- **Path:** `/async`
- **Base URL:** `https://app.bettercontact.rocks/api/v2`
- **Official documentation:** [Create Enrichment](https://doc.bettercontact.rocks/api-reference/endpoint/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[].first_name` | body | `string` | yes | Contact first name for enrichment. |
| `data[].last_name` | body | `string` | yes | Contact last name for enrichment. |
| `data[].company` | body | `string` | yes | Company name for enrichment. |
| `data[].company_domain` | body | `string` | no | Company domain for enrichment. |
| `data[].linkedin_url` | body | `string` | no | LinkedIn profile URL for enrichment. |
| `enrich_email_address` | body | `boolean` | yes | Whether to enrich work email addresses. |
| `enrich_phone_number` | body | `boolean` | yes | Whether to enrich direct phone numbers. |
