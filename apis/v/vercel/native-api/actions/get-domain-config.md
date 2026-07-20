# Get Domain Config with Vercel

Retrieves a domain configuration from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/domains/:domain/config`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Domain Config](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | The domain name to inspect configuration for. |
