# Search Images with Pixabay

Finds images in Pixabay.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/`
- **Base URL:** `https://pixabay.com`
- **Official documentation:** [Search Images](https://pixabay.com/api/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search term to match against Pixabay images. |
| `page` | query | `number` | no | Page number for paginated results. |
| `per_page` | query | `number` | no | Number of results to return per page. |
