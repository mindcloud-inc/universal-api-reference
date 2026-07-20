# Find Email with ZeroBounce

Finds contact emails in ZeroBounce by domain or company.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/guessformat`
- **Base URL:** `https://api.zerobounce.net`
- **Official documentation:** [Find Email](https://www.zerobounce.net/docs/email-finder-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | query | `string` | no |
| `company_name` | query | `string` | no |
| `first_name` | query | `string` | no |
| `middle_name` | query | `string` | no |
| `last_name` | query | `string` | no |
