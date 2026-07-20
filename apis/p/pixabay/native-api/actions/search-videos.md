# Search Videos with Pixabay

Finds videos in Pixabay.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/videos/`
- **Base URL:** `https://pixabay.com`
- **Official documentation:** [Search Videos](https://pixabay.com/api/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search term to match against Pixabay videos. |
