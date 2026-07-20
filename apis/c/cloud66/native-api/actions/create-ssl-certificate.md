# Create SSL Certificate with Cloud 66

Creates an SSL certificate in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/ssl_certificates`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Create SSL Certificate](https://developers.cloud66.com/v3/endpoints/stacks/#ssl-certificates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Unique identifier of the stack |
| `ssl_certificate` | body | `object` | no | SSL certificate payload |
| `server_names` | body | `string` | yes | Comma separated list of domains |
| `ssl_termination` | body | `boolean` | yes | Whether the certificate is terminated on the load balancer |
| `type` | body | `string` | yes | Type of certificate: manual or lets_encrypt |
| `wildcard` | body | `boolean` | no | Only applies to lets_encrypt wildcard certificates |
| `dns_provider_uuid` | body | `string` | no | Required for wildcard lets_encrypt certificates |
| `certificate` | body | `string` | no | Required for manual certificates |
| `key` | body | `string` | no | Required for manual certificates |
| `intermediate_certificate` | body | `string` | no | Intermediate certificate chain |
