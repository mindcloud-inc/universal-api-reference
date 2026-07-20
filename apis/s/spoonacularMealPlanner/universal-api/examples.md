# Spoonacular Meal Planner Universal API Examples

These examples use the MindCloud API key and Spoonacular Meal Planner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Recipes by Ingredients

Finds recipes in Spoonacular Meal Planner by ingredients.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients?connectionId=$CONNECTION_ID&ingredients=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingredients": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "imageType": "string",
      "likes": 1,
      "missedIngredientCount": 1,
      "missedIngredients": [
        {}
      ],
      "title": "string",
      "unusedIngredients": [
        {}
      ],
      "usedIngredientCount": 1,
      "usedIngredients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Search Recipes by Ingredients action reference](actions/search-recipes-by-ingredients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients).

## Add Meal Plan Template

Creates a meal plan template in Spoonacular Meal Planner.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-meal-plan-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-meal-plan-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Meal Plan Template action reference](actions/add-meal-plan-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoonacularMealPlanner/latest/actions/add-meal-plan-template).
