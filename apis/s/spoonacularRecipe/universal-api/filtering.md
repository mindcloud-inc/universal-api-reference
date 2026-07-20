# Spoonacular Recipe Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Spoonacular Recipe expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Spoonacular Recipe actions that support filtering

- [Autocomplete Ingredient Search](actions/autocomplete-ingredient-search.md)
- [Extract Recipe from Website](actions/extract-recipe-from-website.md)
- [Get Random Recipes](actions/get-random-recipes.md)
- [Get Recipe Information Bulk](actions/get-recipe-information-bulk.md)
- [Ingredient Search](actions/ingredient-search.md)
- [Search Recipes](actions/search-recipes.md)
- [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md)
- [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md)
