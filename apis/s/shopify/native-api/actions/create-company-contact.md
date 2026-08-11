# Create Company Contact with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [Create Company Contact](https://shopify.dev/docs/api/admin-graphql/2026-07/mutations/companyContactCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | yes | Shopify Company GID that the contact belongs to. |
| `email` | body | `string` | yes | Email address for the new company contact and associated customer. |
| `firstName` | body | `string` | no | First name for the company contact. |
| `lastName` | body | `string` | no | Last name for the company contact. |
