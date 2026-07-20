# Add Domain with Vercel

Adds an existing domain to Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v7/domains`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Add Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/domains/add-an-existing-domain-to-the-vercel-platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The domain name to add to Vercel. |
