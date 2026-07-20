# List Stories by Tag with lobst.rs

Finds stories in lobst.rs by tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/t/:tag.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [List Stories by Tag](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | path | `string` | yes | Lobsters tag, or comma-separated tags such as rust,programming. |
