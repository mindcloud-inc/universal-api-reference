# List Stories by Category with lobst.rs

Finds stories in lobst.rs by category.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories/:category.json`
- **Base URL:** `https://lobste.rs`
- **Official documentation:** [List Stories by Category](https://github.com/lobsters/lobsters/blob/main/config/routes.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | path | `string` | yes | Lobsters tag category, such as languages, genre, culture, format, or lobsters. |
