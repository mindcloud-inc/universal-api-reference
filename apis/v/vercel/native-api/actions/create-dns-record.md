# Create DNS Record with Vercel

Creates a DNS record in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/domains/:domain/records`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Create DNS Record](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns/create-a-dns-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | The domain name to create the DNS record under. |
| `name` | body | `string` | yes | The DNS record name. |
| `type` | body | `string` | yes | The DNS record type. |
| `value` | body | `string` | yes | The DNS record value. |
