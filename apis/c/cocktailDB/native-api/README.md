# CocktailDB: Native API Reference

A consolidated summary of CocktailDB's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.thecocktaildb.com/api.php
- **API base URL:** `https://www.thecocktaildb.com/api/json/v1/{apiKey}`

## Authentication

### CocktailDB API Key

The provider permits its documented test key for development or educational use. For a public app-store release, obtain Premium access and enter the provider-issued production API key.

### Credentials

- **CocktailDB API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.thecocktaildb.com/api.php)

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Filter Cocktails by Alcoholic Status](actions/filter-cocktails-by-alcoholic-status.md) | `GET /filter.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Filter Cocktails by Category](actions/filter-cocktails-by-category.md) | `GET /filter.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Filter Cocktails by Glass](actions/filter-cocktails-by-glass.md) | `GET /filter.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Filter Cocktails by Ingredient](actions/filter-cocktails-by-ingredient.md) | `GET /filter.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Get Cocktail Details](actions/get-cocktail-details.md) | `GET /lookup.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Get Ingredient Details](actions/get-ingredient-details.md) | `GET /lookup.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Get Random Cocktail](actions/get-random-cocktail.md) | `GET /random.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [List Alcoholic Filters](actions/list-alcoholic-filters.md) | `GET /list.php?a=list` | [docs](https://www.thecocktaildb.com/api.php) |
| [List Cocktail Categories](actions/list-cocktail-categories.md) | `GET /list.php?c=list` | [docs](https://www.thecocktaildb.com/api.php) |
| [List Cocktail Glasses](actions/list-cocktail-glasses.md) | `GET /list.php?g=list` | [docs](https://www.thecocktaildb.com/api.php) |
| [List Cocktails by First Letter](actions/list-cocktails-by-first-letter.md) | `GET /search.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [List Ingredients](actions/list-ingredients.md) | `GET /list.php?i=list` | [docs](https://www.thecocktaildb.com/api.php) |
| [Search Cocktails by Name](actions/search-cocktails-by-name.md) | `GET /search.php` | [docs](https://www.thecocktaildb.com/api.php) |
| [Search Ingredients by Name](actions/search-ingredients-by-name.md) | `GET /search.php` | [docs](https://www.thecocktaildb.com/api.php) |
