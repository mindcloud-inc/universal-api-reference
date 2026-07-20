# List Books By Author End Year with Gutendex

Finds books in Gutendex by author end year.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_year_end` | query | `number` | yes | Upper bound for years when at least one author was alive. |
