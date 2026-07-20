# Update Transaction Metadata with Sharetribe

Updates existing transaction metadata in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `transactions/update_metadata`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Update Transaction Metadata](https://www.sharetribe.com/api-reference/integration.html#update-transaction-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the transaction. |
| `metadata` | body | `object` | yes | Transaction public metadata object to merge at the top level. |
