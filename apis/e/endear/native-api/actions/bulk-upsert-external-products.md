# Bulk Upsert External Products with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Bulk Upsert External Products](https://docs.endearhq.com/docs/bulkupsert-endpoint-guidance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.products[]` | body | `array<object>` | yes | Products for the Endear GraphQL operation. |
