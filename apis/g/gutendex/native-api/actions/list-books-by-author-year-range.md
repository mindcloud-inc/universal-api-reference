# List Books By Author Year Range with Gutendex

Finds books in Gutendex by author year range.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_year_start` | query | `number` | yes | Lower bound for years when at least one author was alive. |
| `author_year_end` | query | `number` | yes | Upper bound for years when at least one author was alive. |
