# List User Stories with lobst.rs

Retrieves stories from lobst.rs by user.

## Endpoint

- **Method:** `GET`
- **Path:** `/~:username/stories.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [List User Stories](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Lobsters username, such as jcs. |
