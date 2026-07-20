# List Books By Author Start Year with Gutendex

Finds books in Gutendex by author start year.

## Endpoint

- **Method:** `GET`
- **Path:** `/books/`
- **Base URL:** `https://gutendex.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_year_start` | query | `number` | yes | Lower bound for years when at least one author was alive. |
