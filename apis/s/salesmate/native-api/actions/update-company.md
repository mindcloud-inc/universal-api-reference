# Update Company with Salesmate

## Endpoint

- **Method:** `PUT`
- **Path:** `/company/v4/:companyId`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Update Company](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Salesmate company ID. |
| `name` | body | `string` | yes | Company name. |
| `owner` | body | `number` | yes | Salesmate user ID that owns the company. |
| `website` | body | `string` | no | Company website URL. |
| `phone` | body | `string` | no | Primary phone number. |
| `otherPhone` | body | `string` | no | Secondary phone number. |
| `currency` | body | `string` | no | Three-letter ISO currency code. |
| `description` | body | `string` | no | Internal company description. |
| `tags` | body | `string` | no | Comma-separated tag list. |
