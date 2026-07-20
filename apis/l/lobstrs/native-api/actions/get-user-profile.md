# Get User Profile with lobst.rs

Retrieves a user profile from lobst.rs.

## Endpoint

- **Method:** `GET`
- **Path:** `/~:username.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [Get User Profile](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Lobsters username, such as jcs. |
