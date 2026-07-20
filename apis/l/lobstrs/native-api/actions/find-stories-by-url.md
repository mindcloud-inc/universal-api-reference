# Find Stories by URL with lobst.rs

Finds stories in lobst.rs by URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories/url/all.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [Find Stories by URL](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Submitted URL to match against Lobsters stories. |
