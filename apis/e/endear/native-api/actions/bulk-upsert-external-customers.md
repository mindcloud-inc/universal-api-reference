# Bulk Upsert External Customers with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Bulk Upsert External Customers](https://docs.endearhq.com/docs/bulkupsert-endpoint-guidance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.customers[]` | body | `array<object>` | yes | Customers for the Endear GraphQL operation. |
