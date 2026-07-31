# Foodish Universal API Examples

These examples use the MindCloud API key and Foodish connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Food Image by Category



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-food-image-by-category?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-food-image-by-category?${params}`, {
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
      "image": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Food Image by Category action reference](actions/get-food-image-by-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/foodish/latest/actions/get-food-image-by-category).
