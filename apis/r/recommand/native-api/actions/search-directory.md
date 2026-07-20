# Search Directory with Recommand

Finds recipients in the Recommand directory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/search-peppol-directory`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Search Directory](https://recommand.eu/en/reference/recipients/search-directory)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The search query to find recipients. |
