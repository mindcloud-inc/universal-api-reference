# Get Story by Slug with lobst.rs

Retrieves a story from lobst.rs by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/s/:shortId/:titleSlug.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [Get Story by Slug](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortId` | path | `string` | yes | Lobsters story short ID, such as hedf1w. |
| `titleSlug` | path | `string` | yes | Story title slug from the canonical Lobsters URL. |
