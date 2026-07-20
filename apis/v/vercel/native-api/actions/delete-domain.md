# Delete Domain with Vercel

Deletes an existing domain from Vercel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v6/domains/:domain`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Delete Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/remove-a-domain-by-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | The domain name to remove. |
