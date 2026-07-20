# List Posts with THE HILL

Retrieves published posts from The Hill.

## Endpoint

- **Method:** `GET`
- **Path:** `/wp/v2/posts`
- **Base URL:** `https://thehill.com/wp-json/`
- **Official documentation:** [List Posts](https://developer.wordpress.org/rest-api/reference/posts/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Sort direction for the post list. |
| `orderby` | query | `string` | no | Sort posts by a WordPress field. |
| `page` | query | `number` | no | Page number to fetch. |
| `per_page` | query | `number` | no | Number of posts to return per page. |
| `search` | query | `string` | no | Search posts by keyword. |
| `slug` | query | `string` | no | Filter posts by slug. |
