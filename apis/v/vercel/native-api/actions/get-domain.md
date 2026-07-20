# Get Domain with Vercel

Retrieves a domain record from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v5/domains/:domain`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/get-information-for-a-single-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | The domain name to retrieve. |
