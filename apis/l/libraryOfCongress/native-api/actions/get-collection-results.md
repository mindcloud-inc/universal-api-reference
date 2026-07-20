# Get Collection Results with Library of Congress

Retrieves results from a Library of Congress collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{collectionSlug}/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Get Collection Results](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionSlug` | path | `string` | yes | The kebab-case loc.gov collection slug, such as civil-war-maps or baseball-cards. |
