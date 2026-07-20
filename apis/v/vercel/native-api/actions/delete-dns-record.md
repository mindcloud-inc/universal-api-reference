# Delete DNS Record with Vercel

Deletes an existing DNS record from Vercel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/domains/:domain/records/:recordId`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Delete DNS Record](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns/delete-a-dns-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | The domain name that owns the DNS record. |
| `recordId` | path | `string` | yes | The DNS record ID to remove. |
