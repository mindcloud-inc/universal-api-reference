# Get Collection Pagination with Library of Congress

Retrieves pagination for a Library of Congress collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{collectionSlug}/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Get Collection Pagination](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionSlug` | path | `string` | yes | The kebab-case loc.gov collection slug, such as civil-war-maps or baseball-cards. |
