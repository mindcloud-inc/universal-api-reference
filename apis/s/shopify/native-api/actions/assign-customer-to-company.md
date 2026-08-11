# Assign Customer to Company with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [Assign Customer to Company](https://shopify.dev/docs/api/admin-graphql/2026-07/mutations/companyAssignCustomerAsContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | yes | Shopify Company GID to receive the existing customer. |
| `customerId` | body | `string` | yes | Shopify Customer GID to assign as a company contact. |
