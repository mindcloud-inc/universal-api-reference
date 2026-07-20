# Search Images with AltText.Ai

Searches images in your AltText.Ai library.

## Endpoint

- **Method:** `GET`
- **Path:** `/images/search`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [Search Images](https://alttext.ai/apidocs#tag/Images/operation/search-images)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search by asset ID, URL substring, or alt text content. |
