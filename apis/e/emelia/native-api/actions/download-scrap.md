# Download Scrap with Emelia

Retrieves a scrap download from Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Download Scrap](https://docs-old.emelia.io/#operation-download_a_scrap-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | yes | Download format integer. Provide a number such as 0 or 1. |
| `id` | body | `string` | yes | Scrap identifier |
