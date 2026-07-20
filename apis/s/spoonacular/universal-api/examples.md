# Spoonacular Universal API Examples

These examples use the MindCloud API key and Spoonacular connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze a Recipe Search Query

Analyzes a recipe search query in Spoonacular.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/analyze-a-recipe-search-query?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/analyze-a-recipe-search-query?${params}`, {
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
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Analyze a Recipe Search Query action reference](actions/analyze-a-recipe-search-query.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoonacular/latest/actions/analyze-a-recipe-search-query).

## Add Custom Foods

Creates a custom food in Spoonacular.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/add-custom-foods" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hash": "string",
  "requestBody": "string",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/add-custom-foods', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hash": "string",
    "requestBody": "string",
    "username": "Ava Chen"
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
      "result": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Custom Foods action reference](actions/add-custom-foods.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spoonacular/latest/actions/add-custom-foods).
