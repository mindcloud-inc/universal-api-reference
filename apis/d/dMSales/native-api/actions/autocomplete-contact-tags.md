# Autocomplete Contact Tags with DMSales

Finds contact tags in DMSales by partial tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/contact-card/autocomplete-tags`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [Autocomplete Contact Tags](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part_tag` | query | `string` | yes | Partial tag text to autocomplete. |
