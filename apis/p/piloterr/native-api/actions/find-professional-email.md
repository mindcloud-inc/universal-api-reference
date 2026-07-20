# Find Professional Email with Piloterr

## Endpoint

- **Method:** `GET`
- **Path:** `/email/finder`
- **Base URL:** `https://api.piloterr.com/v2`
- **Official documentation:** [Find Professional Email](https://docs.piloterr.com/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_domain` | query | `string` | no | Company domain for the email lookup. |
| `company_name` | query | `string` | no | Company name for the email lookup. |
| `query` | query | `string` | yes | Full name of the person whose professional email you want to find. |
