# Find Work Verified Email with Datagma

Finds a verified work email in Datagma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v8/findEmail`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Find Work Verified Email](https://datagmaapi.readme.io/reference/ingressservice_findemailv8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyLinkedinSlug` | query | `string` | no | LinkedIn company URL or company slug used to improve the match rate. |
| `firstName` | query | `string` | no | Target person's first name. |
| `lastName` | query | `string` | no | Target person's last name. |
| `company` | query | `string` | no | Target company name. |
| `linkedInSlug` | query | `string` | no | LinkedIn company URL or company slug used to improve the match rate. |
| `findEmailV2Step` | query | `string` | no | Use 3 to return the email address or 2 for the domain only; both cost the same. |
| `findEmailV2Country` | query | `string` | no | Country hint to improve matching accuracy. Use General if unknown. |
| `fullName` | query | `string` | no | Target person's full name. |
