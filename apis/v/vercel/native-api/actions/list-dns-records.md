# List DNS Records with Vercel

Retrieves all DNS records from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/domains/:domain/records`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [List DNS Records](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | The domain name whose DNS records should be listed. |
