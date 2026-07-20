# Get Comment with lobst.rs

Retrieves a comment from lobst.rs.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:commentShortId.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [Get Comment](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentShortId` | path | `string` | yes | Lobsters comment short ID, such as efgamd. |
