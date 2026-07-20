# Retrieve Brand Data by Domain with Brand.dev

Retrieves brand data from Brand.dev by domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/brand/retrieve`
- **Base URL:** `https://api.brand.dev/v1`
- **Official documentation:** [Retrieve Brand Data by Domain](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain name to retrieve brand data for. |
| `force_language` | query | `string` | no | Optional language to force for the returned brand data. |
| `maxSpeed` | query | `boolean` | no | Optimize for maximum speed at the cost of less comprehensive data. |
| `timeoutMS` | query | `number` | no | Optional timeout in milliseconds for the request. |
