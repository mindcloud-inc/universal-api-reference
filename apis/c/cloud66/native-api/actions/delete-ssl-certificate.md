# Delete SSL Certificate with Cloud 66

Deletes an SSL certificate from your Cloud 66 account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/stacks/:stack_id/ssl_certificates/:id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Delete SSL Certificate](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Unique identifier of the stack |
| `id` | path | `string` | yes | SSL certificate ID |
