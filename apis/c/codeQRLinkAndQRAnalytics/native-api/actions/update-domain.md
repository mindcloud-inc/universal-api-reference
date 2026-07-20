# Update Domain with CodeQR - Link and QR Analytics

Updates a domain in CodeQR.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/domains/:slug`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Update Domain](https://docs.codeqr.io/api-reference/endpoint/update-a-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The domain name. |
| `placeholder` | body | `string` | no | Example link placeholder shown in the link creation modal. |
