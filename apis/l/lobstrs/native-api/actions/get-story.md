# Get Story with lobst.rs

Retrieves a story from lobst.rs.

## Endpoint

- **Method:** `GET`
- **Path:** `/s/:shortId.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [Get Story](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortId` | path | `string` | yes | Lobsters story short ID, such as hedf1w. |
