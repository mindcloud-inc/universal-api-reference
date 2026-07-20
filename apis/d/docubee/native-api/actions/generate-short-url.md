# Generate Short URL with Docubee

Generates a temporary short URL for a Docubee link.

## Endpoint

- **Method:** `POST`
- **Path:** `/urls`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Generate Short URL](https://docs.docubee.app/#generate-a-short-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | no | The full Docubee URL to shorten. |
