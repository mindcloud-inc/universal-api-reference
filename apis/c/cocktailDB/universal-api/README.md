# <img src="https://images.mindcloud.co/apps/icons/cocktaildb_1785426396167.png" alt="CocktailDB logo" width="28" height="28"> CocktailDB: Universal API

Search cocktail recipes, look up drinks and ingredients, and filter the CocktailDB catalog using a production API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cocktailDB/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thecocktaildb.com/
- **Vendor API docs:** https://www.thecocktaildb.com/api.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Filter Cocktails by Alcoholic Status](actions/filter-cocktails-by-alcoholic-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/filter-cocktails-by-alcoholic-status?connectionId=$CONNECTION_ID&alcoholicStatus=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Alcoholic Status

| Action | Method | Description |
| --- | --- | --- |
| [List Alcoholic Filters](actions/list-alcoholic-filters.md) | GET |  |

### Cocktail

| Action | Method | Description |
| --- | --- | --- |
| [Filter Cocktails by Alcoholic Status](actions/filter-cocktails-by-alcoholic-status.md) | GET |  |
| [Filter Cocktails by Category](actions/filter-cocktails-by-category.md) | GET |  |
| [Filter Cocktails by Glass](actions/filter-cocktails-by-glass.md) | GET |  |
| [Filter Cocktails by Ingredient](actions/filter-cocktails-by-ingredient.md) | GET |  |
| [Get Cocktail Details](actions/get-cocktail-details.md) | GET |  |
| [Get Random Cocktail](actions/get-random-cocktail.md) | GET |  |
| [List Cocktails by First Letter](actions/list-cocktails-by-first-letter.md) | GET |  |
| [Search Cocktails by Name](actions/search-cocktails-by-name.md) | GET |  |

### Cocktail Category

| Action | Method | Description |
| --- | --- | --- |
| [List Cocktail Categories](actions/list-cocktail-categories.md) | GET |  |

### Cocktail Glass

| Action | Method | Description |
| --- | --- | --- |
| [List Cocktail Glasses](actions/list-cocktail-glasses.md) | GET |  |

### Ingredient

| Action | Method | Description |
| --- | --- | --- |
| [Get Ingredient Details](actions/get-ingredient-details.md) | GET |  |
| [List Ingredients](actions/list-ingredients.md) | GET |  |
| [Search Ingredients by Name](actions/search-ingredients-by-name.md) | GET |  |

